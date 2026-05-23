## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:31b91afda61114922f389585942bd1722301ce2bf181af36aac5f1e0b9dc45fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:13d325f7dfa50d6ea443f933f74d7418ee5e09a55b8435b535f647119ca541b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **522.3 MB (522259740 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5efbe96ce4cb04d9e9dd5f06762442470fd15e450e15378ab19172afd07655f6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:11:23 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:11:23 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:11:23 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:11:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 May 2026 22:10:01 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 22 May 2026 22:10:02 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 22 May 2026 22:10:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:10:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:10:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:10:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:10:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:10:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:10:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:10:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:10:02 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:10:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:10:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:10:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e164628c07dac6b95a1129a4b9c10a619e5f4780ebd7b5aa462019fee2bd9a`  
		Last Modified: Fri, 22 May 2026 21:12:19 GMT  
		Size: 330.8 MB (330821282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60629e9250ed23c3ae650294f4c49d6cb79ade774ccd56d4e251895d49192596`  
		Last Modified: Fri, 22 May 2026 22:10:30 GMT  
		Size: 122.1 MB (122062988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:146aaf64b6347bff4c653b0705cb7666834939526c89140b01fb9b6077e2ad72`  
		Last Modified: Fri, 22 May 2026 22:10:27 GMT  
		Size: 5.4 MB (5442062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d930a07b172a261be2239eea8c0a4e7446ed6e2a7c9e3eaeb59dae9b4bbab4fc`  
		Last Modified: Fri, 22 May 2026 22:10:27 GMT  
		Size: 9.4 MB (9359960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea7938a15f807057d7fe6047ed7ed8773a52fee6fb3d2d5ac2996725f16de99`  
		Last Modified: Fri, 22 May 2026 22:10:27 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23bc92da4a56519f4ba696435ac06f1a1473401c6f171f8cb599dae5ff680d4f`  
		Last Modified: Fri, 22 May 2026 22:10:28 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:cc74091152414bc1ad2c36425417056cc6773595ff3c952219f9bbc14505da1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52086852693179d42f2c2c123abd75bfc3c0eb0cef7d60d8088178e5d5423549`

```dockerfile
```

-	Layers:
	-	`sha256:7be0e28c2c77b7b8e3a8ea7428d9adad1359b6a1319caf620b0507cecbaac2cb`  
		Last Modified: Fri, 22 May 2026 22:10:27 GMT  
		Size: 13.8 MB (13834663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b16c07b5e4b9d2382ef60c2118b9d515966554c492fdf45b6de2a00ed327d1d1`  
		Last Modified: Fri, 22 May 2026 22:10:26 GMT  
		Size: 16.3 KB (16285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5caf6c7f265e3bb3f80b5e1e5d78629dfa70098fccb8405c8545c04d733c4074
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.0 MB (312015337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60793c45687cc26758dc67508ac948e5212b5147316025256f7be656d9338578`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:10:41 GMT
ARG version=1.8.0_492.b09-2
# Fri, 22 May 2026 21:10:41 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:10:41 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:10:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 22 May 2026 22:10:22 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 22 May 2026 22:10:24 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 22 May 2026 22:10:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 22 May 2026 22:10:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:10:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 22 May 2026 22:10:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 22 May 2026 22:10:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 May 2026 22:10:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 22 May 2026 22:10:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 22 May 2026 22:10:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 22 May 2026 22:10:24 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 May 2026 22:10:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 May 2026 22:10:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 May 2026 22:10:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba004d93628b9d5794265bf99f9a1a771d2977c59482363489cc72908526a674`  
		Last Modified: Fri, 22 May 2026 21:11:02 GMT  
		Size: 118.0 MB (117957852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a5b39d01d0d35b0f69bb0dae349dfa86c72354983d1407a2543478a2b96c6aa`  
		Last Modified: Fri, 22 May 2026 22:10:44 GMT  
		Size: 118.5 MB (118472341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:554dd72a233c390cf30bee11c8eb8deb086b7fa640fe5f5cf61afa62c2c33ad9`  
		Last Modified: Fri, 22 May 2026 22:10:42 GMT  
		Size: 12.8 MB (12769745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e760ad505f6a9b3d8d5d35a3567cddd5db091264bf7c4aea3b13d525c780eae`  
		Last Modified: Fri, 22 May 2026 22:10:41 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ece7d2e19b0c5e65cf1d0a7dca6e45eee65936f18a8f09fe49e47558fe636de1`  
		Last Modified: Fri, 22 May 2026 22:10:41 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5766e6d8c3482133cb426d7b1a42e1255a18939979491db2ba9e924878f914a0`  
		Last Modified: Fri, 22 May 2026 22:10:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:59c3def98804a10750c3446c8d511c09881e0541a923868d2eb12acef46e6654
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e5678355e06f3d6ceeaac3860535e772a174424ddd2132585072508de72e92`

```dockerfile
```

-	Layers:
	-	`sha256:67267b3ae9cacb5cbf6cc77e714bdf89551b4bfdf46d5e8ad00c7424f63ed175`  
		Last Modified: Fri, 22 May 2026 22:10:41 GMT  
		Size: 6.6 MB (6615976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2c5015bd991df5abcf54fcbd5ab7e9d38c8ebb8076473b81094211c2be0df56`  
		Last Modified: Fri, 22 May 2026 22:10:40 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
