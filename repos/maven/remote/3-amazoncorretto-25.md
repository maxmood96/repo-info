## `maven:3-amazoncorretto-25`

```console
$ docker pull maven@sha256:f5ae13f9a73052d770670c7ad2829d2475e63c4bbe26f06f3e8eea162f17d4c0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25` - linux; amd64

```console
$ docker pull maven@sha256:438659f25582c7c6ebd23dabed5f7e5cf1fad400250ff634ee88df3e4778dd02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367867886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbb22de3b6ba83a98e28d5e151b47ca1185bbc70c174224db51542ab8188aa4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:25 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:25 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:25 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 17 Mar 2026 03:48:45 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Mar 2026 03:48:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:48:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:48:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:48:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:48:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:48:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:48:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:48:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:48:45 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:48:45 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:48:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:48:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:48:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1899f99dbf61d2e92bf9bc374b2f4ec7c5b8a1687b8543b4ecc212164833f14`  
		Last Modified: Wed, 11 Mar 2026 18:34:50 GMT  
		Size: 189.2 MB (189186371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a727aa3a3ee88b6f9194dca33ef8a852ceeeaa20a89307f772944a57e5b302`  
		Last Modified: Tue, 17 Mar 2026 03:49:06 GMT  
		Size: 115.3 MB (115336208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfbc9e2030ca0f9c8ef33df28377f9c5d502e169a8acf9e9a3e4353a6f209730`  
		Last Modified: Tue, 17 Mar 2026 03:49:04 GMT  
		Size: 9.3 MB (9311177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf21a0faa9405a39044632dfba452b8d0bb1a4c98c4aaa5a37fe23041d797a3`  
		Last Modified: Tue, 17 Mar 2026 03:49:03 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9deb2a695084daa9917a6ecadf4f79fb31d179697aec29c83d3fba9247ef49e9`  
		Last Modified: Tue, 17 Mar 2026 03:49:03 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:14e3ed85654242f57f4123eda36c90bd7db4e64bdf17483228e94266a9508809
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a98296eaa0cb52d013ac787caf3f406e8187ad28f6a82805063e9a2f48da4158`

```dockerfile
```

-	Layers:
	-	`sha256:438bf2b55633cadb23e24a32178ed95d43f3937d0ad01f820bb5fca2f8d33848`  
		Last Modified: Tue, 17 Mar 2026 03:49:03 GMT  
		Size: 6.2 MB (6209085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c62aef0700ebae1bb599e581a4dbf559f4a0948691929d2c2ba7b2ef365403fd`  
		Last Modified: Tue, 17 Mar 2026 03:49:03 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:822cc9bf144c2c2980206f03d1f5a75690b047e55fbbfdac8135c98518722c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363690981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de9c97616d019419af900a90c25faf0f3893536a8aa70388ad4ca3c8d252b85`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:05 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:05 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:05 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:05 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 17 Mar 2026 03:49:28 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Mar 2026 03:49:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:49:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:49:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:49:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:49:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:49:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:49:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:49:29 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:49:29 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:49:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:49:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:49:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9ab420359a2ce38b24b838a3ea4b4bcbfe85a0c06909eead4a8cca721947cb`  
		Last Modified: Wed, 11 Mar 2026 18:34:30 GMT  
		Size: 187.1 MB (187088807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696b6c7b07eaeda988aaf5d8771b2c9d410797d3debf0cca138257850db90024`  
		Last Modified: Tue, 17 Mar 2026 03:49:49 GMT  
		Size: 114.3 MB (114348583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cacc263282cf6fbd934b3433abf263e3d66a50838e8a18c27be43e51215f397`  
		Last Modified: Tue, 17 Mar 2026 03:49:47 GMT  
		Size: 9.3 MB (9311176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65865c83e7a423ead995eb33a1de503d8d7fac9026a7f439fe2b90da6660930`  
		Last Modified: Tue, 17 Mar 2026 03:49:46 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2831796b554bb69ee4db6b42c2276e81347da62e7242736a1ba63b09f8d4f1`  
		Last Modified: Tue, 17 Mar 2026 03:49:46 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:f15ea1c305d2f61622b683934199b72b73f190b4db85dd973fcc43f2372b7731
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a89b9615efa6be04475e5d85ec39bf346743f76bd2a7dd8091494a093cefeb81`

```dockerfile
```

-	Layers:
	-	`sha256:879769a2c83b8fafebbf83167f72f0b00becb5b95a76a97265aa131346976101`  
		Last Modified: Tue, 17 Mar 2026 03:49:46 GMT  
		Size: 6.2 MB (6208077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:727aa49d6928e16bf9da16d81de91e5378c5fb3f743cae1e67d69a43a9985491`  
		Last Modified: Tue, 17 Mar 2026 03:49:46 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
