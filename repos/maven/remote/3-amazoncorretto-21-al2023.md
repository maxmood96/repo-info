## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:27b9bd8052a0a8e2103b704f79876826baeea30ec27e73467ee8952c2656b7d4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:8fdb87187aedc7292e6e1336cbb4a100e8184f283183069d53bd368a9134ffc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.6 MB (347583094 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24423b30b2126e0e02a5499e999dba672e57529f2248b78cff1a3d44757467f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:01 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:32:01 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:01 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:01 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 17 Feb 2026 22:29:36 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 17 Feb 2026 22:29:38 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:29:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:29:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:29:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:29:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:29:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:29:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:29:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:29:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:29:39 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:29:39 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:29:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:29:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:29:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6774f0a203af37bc6813fc52e095c7d9e0da83df6df12847f411d2cead904a8b`  
		Last Modified: Tue, 10 Feb 2026 18:32:23 GMT  
		Size: 170.2 MB (170192195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12d6fe35875bd0f5b45b97ba4fd059678be8c73fc70bf7f5c49e78bbebe2fec4`  
		Last Modified: Tue, 17 Feb 2026 22:29:57 GMT  
		Size: 101.5 MB (101544163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b66dadca501cf0a174bcedc4f8c4af44deeeb655d9455942fc80573ba1d3b007`  
		Last Modified: Tue, 17 Feb 2026 22:29:55 GMT  
		Size: 12.5 MB (12495233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:512f478a64bd0077979f230828b3f88b23885dd96e2b9435a234c95e071edaf3`  
		Last Modified: Tue, 17 Feb 2026 22:29:55 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c0f95b4f8186990403e0666ccd0ecb6b896ad8724051d0a8873f7bd85dc859`  
		Last Modified: Tue, 17 Feb 2026 22:29:54 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2eda04247a19a1304bf9e950d980b7eaf8b8d4738217c3e8acfb2961fc8d6e`  
		Last Modified: Tue, 17 Feb 2026 22:29:56 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5d1044c6647be606985eee6a2752656e907aec9005f74068460a8a208a9af297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f8e028fdeda71f7fba833e8290387ba261a4780d199b31b1b985736181a6d3a`

```dockerfile
```

-	Layers:
	-	`sha256:e43717acbe3ca948a539884c646c8317e64820c0afd0d5c205a54a70fe7d62bb`  
		Last Modified: Tue, 17 Feb 2026 22:29:55 GMT  
		Size: 6.2 MB (6234451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c91cd1e3e5cfa7357bf0baa4da87db92845e5f363a3ec2e7fc34e0bd03d26f3b`  
		Last Modified: Tue, 17 Feb 2026 22:29:54 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:871b79b91d90376a961ea40d625dfedcd230bf40592e1ac4e70d21da08e5885e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **343.8 MB (343832282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:221f736640155584453f8932179c87a719b60a21443c31f7d49334636307d747`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:53 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:31:53 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:31:53 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:31:53 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Tue, 17 Feb 2026 22:18:02 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 17 Feb 2026 22:18:04 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 17 Feb 2026 22:18:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:18:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:18:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:18:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:18:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:18:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:18:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:18:05 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:18:05 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:18:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:18:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:18:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad4ed46cdf2a663ea36c8c181d3674949b11e5db1ede4dd29e329450b151f56`  
		Last Modified: Tue, 10 Feb 2026 18:32:17 GMT  
		Size: 168.5 MB (168466424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e721bc727c6cb83658aee39e86a3b4ba58ea1ea1a6b0be3a5c8b6f2c77d0c0c`  
		Last Modified: Tue, 17 Feb 2026 22:18:24 GMT  
		Size: 100.4 MB (100378079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fabc1a9d263656d95907979fd9ae0fd48579cdc3c5a5c423bebfec3e340bee0a`  
		Last Modified: Tue, 17 Feb 2026 22:18:22 GMT  
		Size: 12.8 MB (12756282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:708e8577201b7db62ecdc466224ac58a26c7fdc58fe65318b7af60fc41873db2`  
		Last Modified: Tue, 17 Feb 2026 22:18:22 GMT  
		Size: 9.3 MB (9312246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d65e8a4e0689429d5cff07020591239eb6648044131c702b9457e2e2de4532`  
		Last Modified: Tue, 17 Feb 2026 22:18:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53af40a4f67efbf3b6251c13c574bae8c95e5867b8f8d5a9523d22493099b19c`  
		Last Modified: Tue, 17 Feb 2026 22:18:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:0dc586612322febe2fd8e97cbdde7929c9bd5fc928bc9bd342a0da5ebf7b60ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1927b02e1a2c8b03095e3ee2aa8934e733534bc7bd6c82bd76f0ffc50daad035`

```dockerfile
```

-	Layers:
	-	`sha256:aec118394869f47c42a86924177a5ee2d31d3bf40cc78836517f74a5edac2674`  
		Last Modified: Tue, 17 Feb 2026 22:18:22 GMT  
		Size: 6.2 MB (6233384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:939684306e65916d652b9ae76f296d6d69f8d09c5570b3fa5e76f195c1876d3f`  
		Last Modified: Tue, 17 Feb 2026 22:18:21 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
