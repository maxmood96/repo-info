## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:9ceb59987756318e2bf312c2402e517cd2e7644304677c4eee7153402389d7b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:8f3f3cbf1e38f9443c9122c4612f5e37ddea3d4ffb14be363af9c2f52ed3b06d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367867729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77b388adc46a50dd33c4f1a48efa81bf1b970f18ae947ce59938ba586d4eeb9d`
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
# Fri, 03 Apr 2026 17:30:26 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 03 Apr 2026 17:30:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 17:30:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:30:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:30:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 17:30:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 17:30:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 17:30:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 17:30:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 17:30:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 17:30:26 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 17:30:26 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 17:30:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 17:30:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 17:30:26 GMT
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
	-	`sha256:c3acd4a4717c552a44efcaf81ed95d1adb5f415991979a9a13c50609b89b4cc3`  
		Last Modified: Fri, 03 Apr 2026 17:30:45 GMT  
		Size: 115.3 MB (115335964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fa82db8f73b2653cd92937162ebdca9a6b6dff8dc0b716a3d72fad1001feb2`  
		Last Modified: Fri, 03 Apr 2026 17:30:42 GMT  
		Size: 9.3 MB (9311182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f850bc60b497b8e3679efef07558b8855e7ea368ff7bee4dc39d0019f64c947c`  
		Last Modified: Fri, 03 Apr 2026 17:30:42 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b3f72db6087370fb7282317a6807d56c90b4695eb42eba2fa22a883cdfd99e`  
		Last Modified: Fri, 03 Apr 2026 17:30:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:e92dd877aec39f30ec960cb52bd25e73982e567f60827ee0653e93eaaaf327c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c624008f480d26096a7a147d90d44e975f85bb398badd51a80f6995925110623`

```dockerfile
```

-	Layers:
	-	`sha256:d25c87934f26849dbc7223bdcd5813654e9ff89e1433eb8ed02e1986a4fab1e3`  
		Last Modified: Fri, 03 Apr 2026 17:30:42 GMT  
		Size: 6.2 MB (6209085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d956b1376c19dcc4246ddfbcfdcfd1c0cd597a0d9a6f072b71114924a40f0636`  
		Last Modified: Fri, 03 Apr 2026 17:30:42 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6963715cd6be457cfbaf0e7c1b7f011c2b8f4c98fa46c205fb420fdf8bbcee2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363690744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70907e450a0cd66877d72a841dbb0908adbe348161f52486a93400a5c51fa336`
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
# Fri, 03 Apr 2026 17:36:26 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 03 Apr 2026 17:36:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 17:36:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:36:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:36:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 17:36:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 17:36:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 17:36:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 17:36:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 17:36:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 17:36:26 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 17:36:26 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 17:36:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 17:36:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 17:36:26 GMT
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
	-	`sha256:faf310e47ea01cddae7f5116a63207d518c5dcbbf5453ca22db3ce68ad815586`  
		Last Modified: Fri, 03 Apr 2026 17:36:45 GMT  
		Size: 114.3 MB (114348373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e2948aebbe2d067fd0532511cc22f2cb10dea238d7cc9624defefb5ac361e93`  
		Last Modified: Fri, 03 Apr 2026 17:36:42 GMT  
		Size: 9.3 MB (9311186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efdba9040c9aff4c31b1fa199726279502fbc0cd241a04dcfd1f780eb858b23`  
		Last Modified: Fri, 03 Apr 2026 17:36:42 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a8def3c115f791923bd6043756cb75a1e9db6797442197f228469916f845809`  
		Last Modified: Fri, 03 Apr 2026 17:36:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:09964dc43115bcee2cb9d76bd2b7d758c557a40f2d1a8b25a64c2e0d6c919259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5d2ef705b4e1b0beb145bd2c4ad4d7706938b028eb476b00d64b4c5d32a7e1`

```dockerfile
```

-	Layers:
	-	`sha256:0cc2fd69c9e943c06c7e887c9c6768b30d4611ec5e9e5fe6884fea01259f366f`  
		Last Modified: Fri, 03 Apr 2026 17:36:42 GMT  
		Size: 6.2 MB (6208077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fdbca9e1d6a23e5184d4f7ee783de2371f7ef5ebe0e5fc1195c5be29286b3c20`  
		Last Modified: Fri, 03 Apr 2026 17:36:42 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
