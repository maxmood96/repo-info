## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:7f2189cb12c00b1f59716f440522c97685ff95f5ee120966e6e244d3c5715537
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:7e674148a40653735621d9f67dbb8105fc8a42dc53348014a7de78b30dbab83c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354748282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da62fd892f6666eba488a0f1cb57e52c907af8cbd897bffaa339282ed3aff045`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:07:15 GMT
ARG version=25.0.1.9-1
# Wed, 05 Nov 2025 01:07:15 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:07:15 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:07:15 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 05 Nov 2025 05:03:19 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 05 Nov 2025 05:03:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 05 Nov 2025 05:03:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 05 Nov 2025 05:03:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 05 Nov 2025 05:03:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 05 Nov 2025 05:03:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 05 Nov 2025 05:03:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 05 Nov 2025 05:03:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 05 Nov 2025 05:03:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 05 Nov 2025 05:03:19 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 05 Nov 2025 05:03:19 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 05 Nov 2025 05:03:19 GMT
ARG USER_HOME_DIR=/root
# Wed, 05 Nov 2025 05:03:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 05 Nov 2025 05:03:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 05 Nov 2025 05:03:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c1f44d1f333eca771d4302a52c66b724492a443b32096a502dd680573ad6f9`  
		Last Modified: Wed, 05 Nov 2025 04:48:51 GMT  
		Size: 189.2 MB (189168084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ffb7d4cc4c0d27ba4d7860bcad037248e68ce0209ddc2060bce3b4e8573a45`  
		Last Modified: Wed, 05 Nov 2025 05:03:55 GMT  
		Size: 102.3 MB (102335324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09bf06458c22d9195a57716000f6f0247cb850a92fabefc49c02273b8e4feaea`  
		Last Modified: Wed, 05 Nov 2025 05:03:45 GMT  
		Size: 9.2 MB (9242596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7df3631534816bf05fc8c08500598fe07ea48564ecbcbb5e0fd652c3553c854`  
		Last Modified: Wed, 05 Nov 2025 05:03:44 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6e205478ed0c352f17c8a5aab80784f7764841e519671d2e26caddf8948f96`  
		Last Modified: Wed, 05 Nov 2025 05:03:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:5a526c4198406a31cfb94c097573b30680564c31300764ba8c7d0ad0eb6e4866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f55772e8bcf6014a7916d84f7dde6b64faf16e95e6b203849175e651a56b429`

```dockerfile
```

-	Layers:
	-	`sha256:fb6ab6581c097fce65145c95626ec3f4ddfaecc66c5b9d09df60d9c46ed932ed`  
		Last Modified: Wed, 05 Nov 2025 06:27:21 GMT  
		Size: 6.2 MB (6209006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ba4bbf51e8510bea36b9aeed979068640e8f9076eca668c83856bd0f29647fb`  
		Last Modified: Wed, 05 Nov 2025 06:27:21 GMT  
		Size: 17.5 KB (17548 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:949f128b6acc15cfa04b6a9e32dad37601741cb463c8f096c2fbfa5a1d5b3b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350894135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e81d736af915970ad3b98e8eee0a1ad1bdb61fe7af94bf279aa7a5c80ebdf3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:16:48 GMT
ARG version=25.0.1.9-1
# Tue, 04 Nov 2025 23:16:48 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:16:48 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:16:48 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 04 Nov 2025 23:27:19 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 04 Nov 2025 23:27:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 04 Nov 2025 23:27:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 04 Nov 2025 23:27:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 04 Nov 2025 23:27:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 04 Nov 2025 23:27:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 04 Nov 2025 23:27:20 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 04 Nov 2025 23:27:20 GMT
ARG USER_HOME_DIR=/root
# Tue, 04 Nov 2025 23:27:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 04 Nov 2025 23:27:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 04 Nov 2025 23:27:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365c25afe64e4be1bd920de12cba12a4866ebadce41ee02775bebe9869913ec`  
		Last Modified: Tue, 04 Nov 2025 23:25:30 GMT  
		Size: 187.1 MB (187092250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7577b72361f1a7be63cb2cda982b4927a7fe191baea718271a0661de58ed706`  
		Last Modified: Tue, 04 Nov 2025 23:27:57 GMT  
		Size: 101.7 MB (101656406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02497aa030ede5e70b901554496af2bbad6739c447c95ce19bc0403715d06265`  
		Last Modified: Tue, 04 Nov 2025 23:27:46 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab922cb52bb0c9103a479d8d50e591738b1f7557e7f4c3e8dfb331d71d4138b`  
		Last Modified: Tue, 04 Nov 2025 23:27:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c84d4f138ff44da479ba1f0280ead4cb8b3ecd499665483ffcf285b65084e`  
		Last Modified: Tue, 04 Nov 2025 23:27:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:13817ed40b6082ee35c5af2cd79cd87a6edc5f1bd4e11023ce8de14d85866e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3621af07641924d4835d24e3f3d43756d6ade91b83317b8fed8acd20aa5a01b`

```dockerfile
```

-	Layers:
	-	`sha256:0a92d22bc234bd753b8791de75ddaed76d69eee43cdd3fecfc44c947a75b668b`  
		Last Modified: Wed, 05 Nov 2025 00:27:41 GMT  
		Size: 6.2 MB (6207998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9caecad075a2744d6cabed6606c85cccedc7bc5d466608155697c6dfceab9763`  
		Last Modified: Wed, 05 Nov 2025 00:27:42 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
