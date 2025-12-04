## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:e05aefd8532a850d04df2512a08d5df00a8afada7d8d1f50b48b782b7ae72497
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:24b6d5fa361ea5a7e0d146cc501675428408da0976d4ce07a60cdc30f6728f9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.7 MB (322721673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7dd7fad0db8e369a6a0a34bead1a6fd5a4bf3689a5f85987020dc0c5db1874d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:00 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:23:00 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:23:00 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 03 Dec 2025 21:14:43 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 03 Dec 2025 21:14:46 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 03 Dec 2025 21:14:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:14:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:14:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:14:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:14:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:14:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:14:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:14:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:14:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:14:46 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:14:46 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:14:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:14:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:14:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:776c9643cd4150afa1afb3b1c3571d4b01d14b3d59564d8995c086d0ec8c9eb7`  
		Last Modified: Wed, 03 Dec 2025 21:11:23 GMT  
		Size: 153.3 MB (153313008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d637b8511f7b62d3fa983ea7accc2904a2afc5bcacef755ddd36495e29bce5f9`  
		Last Modified: Wed, 03 Dec 2025 21:15:18 GMT  
		Size: 93.7 MB (93704608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09bedfa1383e33c3d634ac325c75bed970ff794bb18f28516aac4c1ceb2186d`  
		Last Modified: Wed, 03 Dec 2025 21:15:11 GMT  
		Size: 12.5 MB (12491414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1971b961881b3fee9610c4e0543212fb7eba351cca470b65b97e1589e654ddd`  
		Last Modified: Wed, 03 Dec 2025 21:15:11 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baa4c47cd5733a82627315f997b9ab98489f55534043a9815f71c0932a5a171`  
		Last Modified: Wed, 03 Dec 2025 21:15:10 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed70b4e1b08b636dc772f4e7e63c2b99762a820d65166f9f6fbfb93aab682cf6`  
		Last Modified: Wed, 03 Dec 2025 21:15:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:dda9c6993958c0582349bca4e74d0d05bca9e25b2a2dfe7f8c668fee960586b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1da27655f77bfc19bddf9858650da3648333fcb36e229250950674e6c275eaa6`

```dockerfile
```

-	Layers:
	-	`sha256:22fb0808874c2b28356f897b1e2170f681aa94ea16916b8ea3093643dab2a3c2`  
		Last Modified: Thu, 04 Dec 2025 00:27:40 GMT  
		Size: 6.3 MB (6257524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e466201596df646dcab7338af37f4afb75dda691da1a5963833adb7ec1e20f52`  
		Last Modified: Thu, 04 Dec 2025 00:27:41 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b72d9a04062e6f4fd88a0f4e0214c2b1b3632722523042aadba1e842f2f44672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.3 MB (319343347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62f81d91cedf94e9b1ece7e10f742dcb099b71f563c6a2d48907bb7d93c47bb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:28:24 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:28:24 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:28:24 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:28:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Wed, 03 Dec 2025 21:15:09 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 03 Dec 2025 21:15:11 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 03 Dec 2025 21:15:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 03 Dec 2025 21:15:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 03 Dec 2025 21:15:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 03 Dec 2025 21:15:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 03 Dec 2025 21:15:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 03 Dec 2025 21:15:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 03 Dec 2025 21:15:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 03 Dec 2025 21:15:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 03 Dec 2025 21:15:11 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 03 Dec 2025 21:15:11 GMT
ARG USER_HOME_DIR=/root
# Wed, 03 Dec 2025 21:15:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 03 Dec 2025 21:15:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 03 Dec 2025 21:15:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8861eb4f7a0b53ecbb0f75902386ed6e16a790f86d286d0c6485f438864cf0c`  
		Last Modified: Wed, 03 Dec 2025 21:11:49 GMT  
		Size: 151.9 MB (151860266 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5803d69385c79675d4c06936471847024afb90ca621c9980f02c9bfc5723705`  
		Last Modified: Wed, 03 Dec 2025 21:15:59 GMT  
		Size: 92.6 MB (92617583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8414ba0bd29a17675c4a5781939abcde1a0165b4293a653716aafc7cd06cc8dd`  
		Last Modified: Wed, 03 Dec 2025 21:15:37 GMT  
		Size: 12.8 MB (12752456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c69b1e7b1c946b1920da467ee086d2e23e1af3fe7c2a57ab6e5c21977de8ea`  
		Last Modified: Wed, 03 Dec 2025 21:15:38 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30efb64b132299ab2e66aecf1fd9b1b92eef07e6419c779a6cb96ba8102b8545`  
		Last Modified: Wed, 03 Dec 2025 21:15:36 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce4097806d3e5101595a21f6a86c18bc97b3390e7dfe933db2e4c05838cfea40`  
		Last Modified: Wed, 03 Dec 2025 21:15:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:882c09f7f0264850b95c55d902d50267a5063f2852132260d8b98b7439f20cc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd96dd3d773a2be7b09c2c3fd4844f347e544a128dce470c7ad522c15dc2fbd`

```dockerfile
```

-	Layers:
	-	`sha256:d672c1fa01b4694a53a77fa3ea68b3438670536dc723b339e6ac2d1124a78943`  
		Last Modified: Thu, 04 Dec 2025 00:27:48 GMT  
		Size: 6.3 MB (6257298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e14a750883b46ecb573caf8958ae19a7973c4becbfb941942a103b7a8ed3ef2`  
		Last Modified: Thu, 04 Dec 2025 00:27:49 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json
