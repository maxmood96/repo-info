## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:a66d84257fb71fa9c28f54ed812393c9f159aa0e9ad3ee0bda6288d4424d4c2d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7e285ae4172b731bfe19f64cdefc0fdec39e4dd49c02ea8d0ebe854ae3e4fe50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367867873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c4d7d279243a11ea1017f8f67b80f0c54c8811869e47c9e27db86dfe324d67`
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
# Tue, 17 Mar 2026 03:49:06 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Mar 2026 03:49:06 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:49:06 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:06 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:06 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:49:06 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:49:06 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:49:06 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:49:06 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:49:06 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:49:06 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:49:06 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:49:06 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:49:06 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:49:06 GMT
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
	-	`sha256:9481024e2c397f27106c2d0840fb4588992b99830d057bef6e9d28da58bb88b2`  
		Last Modified: Tue, 17 Mar 2026 03:49:26 GMT  
		Size: 115.3 MB (115336185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:869216c5723bf9e4d2071de06b9fedcf95c7fdd6f9831192cb8fc72f9b7b2f47`  
		Last Modified: Tue, 17 Mar 2026 03:49:24 GMT  
		Size: 9.3 MB (9311187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44dd6e691ed4f308ede346db443317c3d8181345e0dafd595763e9ee97da4c12`  
		Last Modified: Tue, 17 Mar 2026 03:49:23 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9af14b434ad6c810a4773d5d2182ba272816d2007191899e01a9147a6e733f7`  
		Last Modified: Tue, 17 Mar 2026 03:49:24 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:b2af149480c34e936ecb4186838ab6ce4b8168639f4e3ff7665570011d7eac35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25e5f10bf20bdfb1649b5f41a7165899de82d5934ce8db25f2dfa932125b7197`

```dockerfile
```

-	Layers:
	-	`sha256:9f0ac4e5a751c663f6217f074ecd49687c9bcad2498f484f9727ddc7cb068a54`  
		Last Modified: Tue, 17 Mar 2026 03:49:24 GMT  
		Size: 6.2 MB (6207853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf36607677c3cda1ac0cfc879dbee56b41b4e95bb9cab17d1ec3372515bb966e`  
		Last Modified: Tue, 17 Mar 2026 03:49:23 GMT  
		Size: 16.3 KB (16349 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4dfa17606ff7d4eee57dc3d04ce8e8737e2241a94b7f9db8a3984b9d8f5fc319
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363691080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6557fc409245583b690016428d08613f35e623f6ab29c41576a22dd565154fe7`
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
# Tue, 17 Mar 2026 03:49:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Mar 2026 03:49:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Mar 2026 03:49:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Mar 2026 03:49:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Mar 2026 03:49:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Mar 2026 03:49:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Mar 2026 03:49:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Mar 2026 03:49:39 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Mar 2026 03:49:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Mar 2026 03:49:39 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 17 Mar 2026 03:49:39 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Mar 2026 03:49:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Mar 2026 03:49:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Mar 2026 03:49:39 GMT
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
	-	`sha256:5d54b77d63e03da2e87002a6ba9b14cd84f9214d9f9c067d54d08923d69400e5`  
		Last Modified: Tue, 17 Mar 2026 03:49:59 GMT  
		Size: 114.3 MB (114348683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:885402da40a1049641b0fe4a86b2565537841b96ca1e72f2529c5375b7840456`  
		Last Modified: Tue, 17 Mar 2026 03:49:57 GMT  
		Size: 9.3 MB (9311177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6f41db7481833a3e23e0c462857e31511c9a352d5212a7566528fd49e19ae93`  
		Last Modified: Tue, 17 Mar 2026 03:49:56 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b3c89d4c1934425ea494971358dc31639b2ed0c192eec95a0f7304112b1d40`  
		Last Modified: Tue, 17 Mar 2026 03:49:56 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e69604b01969ab55123fcd530690081663feb3180d6e1f21c4744f55b23b8613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6700278b6fb9950eda95d66a98e3ba7a4d2ee0032b234f1014c1c4b211580a35`

```dockerfile
```

-	Layers:
	-	`sha256:fc7bdcc0482fe0f8fe8e7d9a02c0f157016a45ad6bd858c7e79b7a6ecc6473ee`  
		Last Modified: Tue, 17 Mar 2026 03:49:57 GMT  
		Size: 6.2 MB (6206797 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcf1073463650506d0dfa909622d2ecdf76f30a934a24c0da472d36a1ace33fa`  
		Last Modified: Tue, 17 Mar 2026 03:49:56 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
