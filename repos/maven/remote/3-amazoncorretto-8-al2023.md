## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:d46a8022ca566520f01c1167dda01b12bf849c5c0816cb511c4dd1aa5c60ec16
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:f2151e8b74d927acc5572fe99b2398c1548f8092e05f127690cd916a07f5ec2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.0 MB (507997935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:746b78f44e5f014308ebd43fc0773c4f6a89793d32fa5d73c21d47b7c81781d8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:31 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:32:31 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:32:31 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 11 Mar 2026 19:17:21 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 11 Mar 2026 19:17:22 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:17:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:17:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:17:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:17:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:17:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:17:22 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:17:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:17:22 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:17:22 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:17:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:17:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909450d35fc1c76be354ea2673b9c5da1deb7923c5b5712b97182d0002a2807d`  
		Last Modified: Wed, 11 Mar 2026 18:33:28 GMT  
		Size: 330.9 MB (330929370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e06765858e7dc5e942369e57c16d5ebe5c22f55efe65916d001eeb0c7159c6e`  
		Last Modified: Wed, 11 Mar 2026 19:17:50 GMT  
		Size: 107.9 MB (107880290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13f0b3e6bb575526052ad47fd5a45bbd7373ae00ed98053592070eabf3599ff9`  
		Last Modified: Wed, 11 Mar 2026 19:17:47 GMT  
		Size: 5.5 MB (5456625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b575c141de905af2ef9a9e33d5da55c895f7386e32ec89765d6ff465f6b43ad`  
		Last Modified: Wed, 11 Mar 2026 19:17:47 GMT  
		Size: 9.7 MB (9697517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99d016f00da8ba57278c85722e702d8f2f1890d736896b4d8ddca0b265eb66a9`  
		Last Modified: Wed, 11 Mar 2026 19:17:46 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92b5a1784a46d9b19d09c3fb01cbcf3e228276c7a463c06944622218e1162cfd`  
		Last Modified: Wed, 11 Mar 2026 19:17:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1539f464e3e6ac353e5d7f9f8fd5aee2875af8b6fddbca484b7516d3929f9859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13853049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd6ba36139be0a205a758edfb6cc37cb87154d7398aa6482386ed31bf2bb583`

```dockerfile
```

-	Layers:
	-	`sha256:2334df22bd62c9e8459ea630885a243f8801dba05c25f680b2de9eb0f0b3a44a`  
		Last Modified: Wed, 11 Mar 2026 19:17:47 GMT  
		Size: 13.8 MB (13834767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:197f3968dac078dc7ca3fa61926c788dd6d7ce833bf4ce605cc00ae2a56764a0`  
		Last Modified: Wed, 11 Mar 2026 19:17:46 GMT  
		Size: 18.3 KB (18282 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:42515d611ff3d7fe4472994e0400874e99fca961bfb9e9fce6219d913be0898f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **297.6 MB (297637071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d45d3846f8136845239d783506a26d2da2b9a054c7b7eda5d58543695d02e3d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:32:27 GMT
ARG version=1.8.0_482.b08-1
# Wed, 11 Mar 2026 18:32:27 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:32:27 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:32:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 11 Mar 2026 19:17:32 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 11 Mar 2026 19:17:34 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 11 Mar 2026 19:17:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:17:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:17:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:17:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:17:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:17:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:17:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:17:34 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:17:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:17:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:17:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39f17059b29e8ec358b87ff8ec35c787412a89719a8e5af01252dfb3ffccc8e6`  
		Last Modified: Wed, 11 Mar 2026 18:32:46 GMT  
		Size: 118.0 MB (117964262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edb9047d2c2a4621fffc50ec9c8b9c6432ada20acd5530ad4128d876bad4f8a`  
		Last Modified: Wed, 11 Mar 2026 19:17:52 GMT  
		Size: 104.3 MB (104257294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c3bb0c9c90d4fb318a41be88fb85b2a6b1a6a3e815c72f078e5a0d04c8d8d9d`  
		Last Modified: Wed, 11 Mar 2026 19:17:50 GMT  
		Size: 12.8 MB (12775523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c3c8bfd8bb052bac187c6cf0a79f4c7d64cc6c4451df2268b7a4e7e5e5b078`  
		Last Modified: Wed, 11 Mar 2026 19:17:50 GMT  
		Size: 9.7 MB (9697574 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b09401519a102d08112459e3510070b4566f5f6c010c021abb3c474b450dd1`  
		Last Modified: Wed, 11 Mar 2026 19:17:49 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ab37e962bdd6a02403b6db520b2a04be83d465b1d11af16e082584977841810`  
		Last Modified: Wed, 11 Mar 2026 19:17:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:b0a23c7e5c44a5cdc0a0c4c56254cc7ebc4242115ac418d2c7b0d92488165d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24fa3c66b7b316be0738ad4f41ce43c526f56db39ca23d27a49b97fc35ab1e26`

```dockerfile
```

-	Layers:
	-	`sha256:fcfb8743e566310bff0bd05252b6647536408bc9e7f061eb60bb4bc865ef18b0`  
		Last Modified: Wed, 11 Mar 2026 19:17:49 GMT  
		Size: 6.6 MB (6616088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c84640e0139e4eba20913a252802289957d7efa7c7bcbf2cc3c70a9c52640c66`  
		Last Modified: Wed, 11 Mar 2026 19:17:49 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json
