## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:e33256ce8f1aeb99ffac6b273787fb1ef9a07bf1ae4a155116622a7c16da5f0d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:8804ad1d8dd076b4f5c3410b595f7b91e41f38380eedb8f77b5bed565e92bc78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291479821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89e0aef7867c1d7c39bcde8d3773a2c793866389aeec16496fdd1776f9f97627`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de8e0daf47f52b4f98e8194a79247bd4d0a5e85e65498ef67f1439ac1dea1636`  
		Last Modified: Thu, 23 Jan 2025 18:27:35 GMT  
		Size: 156.5 MB (156534342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ada4c65cac25af7699338928cf6604d465bf6cd8aa8872b2367e66611676332`  
		Last Modified: Thu, 23 Jan 2025 20:26:36 GMT  
		Size: 60.1 MB (60082584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:405d0e312a5561a5a2023594eb03d43c097ef15cadf7320936ef0401fb32a159`  
		Last Modified: Thu, 23 Jan 2025 20:26:36 GMT  
		Size: 12.5 MB (12540941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81fe7e45275a7d2c8bf0c255d546928b4060b28116623edb1bcf6974c3a7ed98`  
		Last Modified: Thu, 23 Jan 2025 20:26:35 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528d5d864293cd123fd1e6da314011842131af94dea58af17545b4fc2b4e5edd`  
		Last Modified: Thu, 23 Jan 2025 20:26:34 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:902bd2fdfe2a1f026d478a385d8797589b3c033720701a6c3f11b11802db892a`  
		Last Modified: Thu, 23 Jan 2025 20:26:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:67865b24912ccc9c42e0a50c8b6028fbd22803f527cf1cefa7c57f25daf489a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:485849f9b47c644db72c775ae48abf1d3ea41014cef854d5e0c586872b9eefcb`

```dockerfile
```

-	Layers:
	-	`sha256:3314a4b9c4493245a1a56213d40def05968f181355cd36efdf10e0e741467d76`  
		Last Modified: Thu, 23 Jan 2025 20:26:34 GMT  
		Size: 6.2 MB (6223465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f3c86efce26901214be596ea9279f15ea6ffecbae79245b1487ee480623c5c5`  
		Last Modified: Thu, 23 Jan 2025 20:26:34 GMT  
		Size: 18.3 KB (18317 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:796255e0aa37a17d4f16d5789ade693e107b240b6b9b4aa6ff128a3a72bc582a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **289.2 MB (289192899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22759eb09d9763419fcdc7d17aa07c17b84835903903563c06b49ca3e78d77d1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.14.7-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d09f4dbc6dc3767710290cb0910f5c075928617b8c51bafccaefabb89462ab8`  
		Last Modified: Thu, 23 Jan 2025 18:42:47 GMT  
		Size: 155.4 MB (155380924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:148ef51a62eb63eaa3a6d7279471652c29f9f176ac8873c76bbc3c402cc2a199`  
		Last Modified: Thu, 23 Jan 2025 19:57:10 GMT  
		Size: 59.6 MB (59564747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09252eacc2a106b0c8d3a8de9088807537e440fa9ffda22c21096876cd0bcd03`  
		Last Modified: Thu, 23 Jan 2025 19:57:08 GMT  
		Size: 12.8 MB (12807553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:089df70cbf127965bcb6e46fdc6e6cfbdc29ca15c8f5b3d52d7d19ef2cf5f77b`  
		Last Modified: Thu, 23 Jan 2025 19:57:08 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9233b9c6c5ce9975d88f349b33e6bb64e13a228d3d374e54f769c1dda477456f`  
		Last Modified: Thu, 23 Jan 2025 19:57:08 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb931a819c1df524b351b621941daaaf0569d30bb3f1e0a359cad78dc536a663`  
		Last Modified: Thu, 23 Jan 2025 19:57:09 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:341046b5e9f01d438f4a7d39e34f323661b9374f4e83b833cebcea767d10b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6240860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d920d6ee7d5ce511a3cbab6ba661060611e66d6392c59c1f11b3e63603aa154`

```dockerfile
```

-	Layers:
	-	`sha256:b7572ba3a4f5d8d39921487301f5cea9dd4bd2a37c315372fcc408a11a3a87c2`  
		Last Modified: Thu, 23 Jan 2025 19:57:08 GMT  
		Size: 6.2 MB (6222395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d2302ed6f39e81c549f096f594d36b8bdc77e2e5c24f26be28a4880766723b4e`  
		Last Modified: Thu, 23 Jan 2025 19:57:07 GMT  
		Size: 18.5 KB (18465 bytes)  
		MIME: application/vnd.in-toto+json
