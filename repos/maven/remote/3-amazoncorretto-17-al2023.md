## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:ca99e7876a454b241e013dd5bf550d96e3b2be283ac61dc38bb1e2bee8aefaac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:a6f7c63d6601e05ae985e496705579bf05b1c3c50b1c1bb661f31537df9f3224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.6 MB (342632764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcd792ae2154e5dd6bd4094b414af0b7e98eb0efc780d2dd701454c116139628`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:10 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:10 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:34:10 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:34:10 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Apr 2026 22:14:51 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 22 Apr 2026 22:14:53 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 22 Apr 2026 22:14:53 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 22:14:53 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:53 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:53 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 22:14:53 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 22:14:53 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 22:14:53 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 22:14:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 22:14:54 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 22:14:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 22:14:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 22:14:54 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d90e2e2edb2aa41ddb1bccceaa07382b3ea269f7c64bb96c2c732d22a0e3a7`  
		Last Modified: Wed, 22 Apr 2026 21:34:33 GMT  
		Size: 157.2 MB (157159321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c747ce3b83567530f679620bcda69c119b31149ec84fc87faed544f01507061b`  
		Last Modified: Wed, 22 Apr 2026 22:15:13 GMT  
		Size: 109.1 MB (109056602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:566a4649030b5f5359534ff11f118ec57f678e2e6b423de0630193959623c03a`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 12.5 MB (12532359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22c0a40d8fa523b1e148b0941ef8dd4f1ff57e5dd65f90e27b798b44daf1ea35`  
		Last Modified: Wed, 22 Apr 2026 22:15:12 GMT  
		Size: 9.3 MB (9312216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d20e1ae4cd0579764843d2dd9fa44c44038e4b6da1fe1cf9164814fd3586ca26`  
		Last Modified: Wed, 22 Apr 2026 22:15:09 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c123276389ed079cce50fb392e55b395fce9c5b85afea96905048b462cde85`  
		Last Modified: Wed, 22 Apr 2026 22:15:11 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5a8b5a8972916aacddd592f110dfb379120248c9c664928292780494e974cfab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe69c63fe9529be5293a4e8fa2c7cbfb5fae5ec5637601e42fe778b639949566`

```dockerfile
```

-	Layers:
	-	`sha256:f8a90a4e0d74cc5b202eb9791caf07a51c430896de862e447dbef307c128d5a9`  
		Last Modified: Wed, 22 Apr 2026 22:15:10 GMT  
		Size: 6.2 MB (6239286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b6031d1d5a9982c36750b3ca8bfcb1147443e67047760cefc23f7ff873e5bc`  
		Last Modified: Wed, 22 Apr 2026 22:15:09 GMT  
		Size: 16.3 KB (16289 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:45ffa24f01c8eb4dd396ae855e9d607342a1a5459724162a436d8a5b62681b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.4 MB (339440495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14e34794dad6c1d3ad7cd18bc73c6134557f9b4a392f93ca5d1ba981efbf2cd7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:34:12 GMT
ARG version=17.0.19.10-1
# Wed, 22 Apr 2026 21:34:12 GMT
ARG package_version=1
# Wed, 22 Apr 2026 21:34:12 GMT
# ARGS: version=17.0.19.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:34:12 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 22 Apr 2026 22:14:47 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 22 Apr 2026 22:14:49 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 22 Apr 2026 22:14:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 22 Apr 2026 22:14:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 22 Apr 2026 22:14:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 22 Apr 2026 22:14:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 22 Apr 2026 22:14:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 22 Apr 2026 22:14:50 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 22 Apr 2026 22:14:50 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 22 Apr 2026 22:14:50 GMT
ARG USER_HOME_DIR=/root
# Wed, 22 Apr 2026 22:14:50 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 22 Apr 2026 22:14:50 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 22 Apr 2026 22:14:50 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0561ca8443bb1344561bc8f39e7693dcf5fc60e5a67bf037c5888d8dcde2943`  
		Last Modified: Wed, 22 Apr 2026 21:34:34 GMT  
		Size: 156.0 MB (155990837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483be75c7b345592ebc4b73c5fd404cde1a454efe6d5fda5501ce292d348fc5e`  
		Last Modified: Wed, 22 Apr 2026 22:15:09 GMT  
		Size: 107.9 MB (107903701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60660251a66d1c3d89d30e38ef8e46d1b336a49d5964964eb16efc2e0e5a4e91`  
		Last Modified: Wed, 22 Apr 2026 22:15:07 GMT  
		Size: 12.8 MB (12789950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e5c219e3552283a54355ae110cb1af8f68337153332ab841a30f36b6adc284`  
		Last Modified: Wed, 22 Apr 2026 22:15:07 GMT  
		Size: 9.3 MB (9312258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46b9421eb093114e45e24816ecdc5195a5a6e0413712aadabbc785bba674ec74`  
		Last Modified: Wed, 22 Apr 2026 22:15:06 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7134932f6189bb3b08a14f153fa4cd1d7594a5fd90a6840af8ed1e4647c487be`  
		Last Modified: Wed, 22 Apr 2026 22:15:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:725e0a3701b67588510e5a499ed54699d0c7d9793af866a46dd2169c921f946e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd7e5b4e13a11f85697902f7cd695a38599bf61e35044935c594ec496ef721ef`

```dockerfile
```

-	Layers:
	-	`sha256:a269c29009008a39d9a544649de475b837bd720412def190e0a1915502359679`  
		Last Modified: Wed, 22 Apr 2026 22:15:06 GMT  
		Size: 6.2 MB (6238217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71480613ebe76ed340d6b8fee01ce6fa38c2506bf363df23d55b2f0fbc24d976`  
		Last Modified: Wed, 22 Apr 2026 22:15:06 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
