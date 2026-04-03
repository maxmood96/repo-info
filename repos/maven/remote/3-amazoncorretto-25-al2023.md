## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:dff6ee6334b2155c26b4b9d7d658456d28f931f4e44e55ac4c23003deaffaf73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:900d0a765341c357115bfa07b38cfe842ab5f758fcc6ff443973ca4fbcf5cb37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367867909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a55bfa296956fa84ba64b912cfbfbffadbe496d014d2ed32cbd6a0e1fe92857`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:10:18 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 17:10:18 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:10:18 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:10:18 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:10:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 03 Apr 2026 17:30:27 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 03 Apr 2026 17:30:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 17:30:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:30:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:30:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 17:30:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 17:30:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 17:30:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 17:30:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 17:30:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 17:30:27 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 17:30:27 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 17:30:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 17:30:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 17:30:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:813cb1181068595b4b3c62de5cade14cb611ae97e31a9fb074d6baf78227f42e`  
		Last Modified: Fri, 03 Apr 2026 17:10:41 GMT  
		Size: 189.2 MB (189186449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f741b9989b62902f0ec791cd722b6a4c54a8d171845bcaf7fb3ad82166df5b27`  
		Last Modified: Fri, 03 Apr 2026 17:30:46 GMT  
		Size: 115.3 MB (115336141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4554377564123e63466b72adf7e116c5f88ddee7d6304f781e3b1749c5a3621e`  
		Last Modified: Fri, 03 Apr 2026 17:30:44 GMT  
		Size: 9.3 MB (9311182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95d347d7777c9fb4dbfd5a86f4b5ebbf74cde9f3de60854a2494b62eb06db5b6`  
		Last Modified: Fri, 03 Apr 2026 17:30:44 GMT  
		Size: 855.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416cfa0e864d5ec382c816586865ec5864782bfae98245507051eb5a4b55405a`  
		Last Modified: Fri, 03 Apr 2026 17:30:43 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8a0c68f18674a18666ff15cdc8a2f752dc932bdf3f03b5dbcd59ec7fe4eaefd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275a4cd3f84302c603e0eb25ed5d570deb4225a65d4310cc1281dc09aacf4013`

```dockerfile
```

-	Layers:
	-	`sha256:240f82df51cda469e8d4a5e639a40758b232cd0e95ff243e435202f34f42b1ef`  
		Last Modified: Fri, 03 Apr 2026 17:30:44 GMT  
		Size: 6.2 MB (6207853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7991c60ea2d72e1258d1813ab4af811427e23cef29b9661c597d8173793e5a48`  
		Last Modified: Fri, 03 Apr 2026 17:30:44 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d568a8230c5ebb5a87ba711d3ec323658c16a6b698609d28891dbab5a3b761e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363690802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d3b63b8daaae8e47ca837f8f74ae4d2ea0ea1c933a5d18501c1e919ce69b396`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:17:46 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 17:17:46 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:17:46 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:17:46 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:17:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 03 Apr 2026 17:36:36 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 03 Apr 2026 17:36:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 17:36:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:36:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:36:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 17:36:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 17:36:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 17:36:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 17:36:36 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 17:36:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 17:36:36 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 17:36:36 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 17:36:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 17:36:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 17:36:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e45741ae0b27e627f0eba637c0a75632e9e5e77ba4339c451385c529ee8eb6`  
		Last Modified: Fri, 03 Apr 2026 17:18:11 GMT  
		Size: 187.1 MB (187088766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c2a135fe5bc6f3fadb80146d0894b5cf2ece9231719db7bdbde29aa9c6ca719`  
		Last Modified: Fri, 03 Apr 2026 17:36:59 GMT  
		Size: 114.3 MB (114348441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8255146fe9837523faa0a3ff9400264025a9d6bc22d3122f237ffafd99f3075a`  
		Last Modified: Fri, 03 Apr 2026 17:36:54 GMT  
		Size: 9.3 MB (9311175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5a6641844720d50756cc3dcdfa7d5bd58adaf6a09a83f7526ea711f545f143f`  
		Last Modified: Fri, 03 Apr 2026 17:36:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db587bb5c3f6696f9deb2bd020db0590295505e18b5d0c1cdd12d7d152a51ecf`  
		Last Modified: Fri, 03 Apr 2026 17:36:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e8e5b7b643fd564c0a350cef0e4f4f1582e1815c51255966cf46585108f96b2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96f2b174d11f6969221c2627e7c346c828a6b2b004054fedc20b3abdbad2c2c3`

```dockerfile
```

-	Layers:
	-	`sha256:c98f345a0701ad8d9aaf30ad77f97b662f103a78368ebb22973eabaac2b29626`  
		Last Modified: Fri, 03 Apr 2026 17:36:54 GMT  
		Size: 6.2 MB (6206797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91eb923629caf21634401c52c83b028343e4b2fd9347b07eb3aa4b096784e5bf`  
		Last Modified: Fri, 03 Apr 2026 17:36:54 GMT  
		Size: 16.5 KB (16482 bytes)  
		MIME: application/vnd.in-toto+json
