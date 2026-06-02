## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:58e1cb236c6cdc8ddbe79510be30addfde179527a2fbcee438b432f9948e4eca
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:25eaa7632561b90692f1a81a5d989e66718f1d669b3d24fab58c611771ad2523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.2 MB (351247811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93a6a13c17aa381983705ccc791957e6128ade49d15eef485bac04eb022b5d9f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:26:56 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:26:56 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:11 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:11 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:11 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 02 Jun 2026 10:23:32 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 02 Jun 2026 10:23:33 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:23:33 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:23:33 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:23:33 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:23:33 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:23:33 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:23:33 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:23:33 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:23:33 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:23:33 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:23:33 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:23:33 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:23:33 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2c301665885e6ad3943c3d90b6300031bffd77f1526c8e1fb4fcff7a8956e38`  
		Last Modified: Sat, 30 May 2026 01:11:32 GMT  
		Size: 153.5 MB (153471531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24e47b051c9a3c59444b8e9213c7e9e5432af085755f2b30eeecaddb5274ac4`  
		Last Modified: Tue, 02 Jun 2026 10:23:52 GMT  
		Size: 121.3 MB (121315139 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84f8d7eb3a4df91f0ef818d23eb01d9bbd29edc28ada65996bffad00786a9edc`  
		Last Modified: Tue, 02 Jun 2026 10:23:50 GMT  
		Size: 12.5 MB (12529013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7306f4d09a2fb897376d641488f579e2125d68518812adbdae5dfb44466aa6a`  
		Last Modified: Tue, 02 Jun 2026 10:23:50 GMT  
		Size: 9.4 MB (9359965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25384b21f7fa5be0d4c4a7d92fa5109f885ed3c31b5e38955ef154ef59e31747`  
		Last Modified: Tue, 02 Jun 2026 10:23:49 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f2f70f03750ea7974aa0b04ec1b00e9577b3c349bbe52f3e35f6ccbdf1f35e`  
		Last Modified: Tue, 02 Jun 2026 10:23:51 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:c7cd42ea25e998d665974afb821329b770bfe6df70b5a63fc8714e12c55ae340
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:191cb1a0dc3a3ece37de3a9b254b9fcaf6c99cd2049800573c1d80975e525e61`

```dockerfile
```

-	Layers:
	-	`sha256:1b07d3594a4209cc2ba1f302008f30b7ccd568c597cb7ca7fa12410bc4bd325b`  
		Last Modified: Tue, 02 Jun 2026 10:23:50 GMT  
		Size: 6.3 MB (6263980 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:50300397ef4a51731ffe927f137731ba1eb8c23196af19204e99a98905436153`  
		Last Modified: Tue, 02 Jun 2026 10:23:49 GMT  
		Size: 16.3 KB (16288 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b95a664276d9df07508670169e1135af65235e27532f1a2fc7d74059c43a80fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.6 MB (347603037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df3ce28337ef0ec04190d314e593e7e440f314b094c0959346837ffebcc081db`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 30 May 2026 00:29:22 GMT
COPY /rootfs/ / # buildkit
# Sat, 30 May 2026 00:29:22 GMT
CMD ["/bin/bash"]
# Sat, 30 May 2026 01:11:29 GMT
ARG version=11.0.31.11-1
# Sat, 30 May 2026 01:11:29 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 30 May 2026 01:11:29 GMT
ENV LANG=C.UTF-8
# Sat, 30 May 2026 01:11:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 02 Jun 2026 10:20:39 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 02 Jun 2026 10:20:41 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 02 Jun 2026 10:20:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 02 Jun 2026 10:20:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:20:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 02 Jun 2026 10:20:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 02 Jun 2026 10:20:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 02 Jun 2026 10:20:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 02 Jun 2026 10:20:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 02 Jun 2026 10:20:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 02 Jun 2026 10:20:41 GMT
ARG USER_HOME_DIR=/root
# Tue, 02 Jun 2026 10:20:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 02 Jun 2026 10:20:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 02 Jun 2026 10:20:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f79fb9911ea68ee16566e2d860d6457ab071bbc028d8cd54cc7be3f1495db6`  
		Last Modified: Sat, 30 May 2026 01:11:51 GMT  
		Size: 152.0 MB (152048594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6918f45224d6b21b1c96afc461a8e9c7f517ef17130569e18faf0fe1c3fac3f1`  
		Last Modified: Tue, 02 Jun 2026 10:21:02 GMT  
		Size: 120.0 MB (119951055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcf2fbd85568e23e9284ee926f155bd53f891cdcc556228ff39d809cb9a0807`  
		Last Modified: Tue, 02 Jun 2026 10:20:59 GMT  
		Size: 12.8 MB (12784589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdd00c034e27f4173ee8629ee04b4134c2ab4337fcf79d2b32d936b628f4a87b`  
		Last Modified: Tue, 02 Jun 2026 10:20:59 GMT  
		Size: 9.4 MB (9359962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:436d884108de531066fd3d3da522efce210229343eb7c3b05342e013e37891da`  
		Last Modified: Tue, 02 Jun 2026 10:20:58 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da64471665a83d33bd5d047923c34ca190df5be470be6db7d957f25736f6abfe`  
		Last Modified: Tue, 02 Jun 2026 10:20:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:aab15f9022d7548198fa6700fdccb7b167fdcc84c41222a9f36c8d11063a26c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925fdf969de54d1544f5c111403d4a7f80c6e42ca60d6ad4e106087cfb6d1ec0`

```dockerfile
```

-	Layers:
	-	`sha256:6967ead7aa54765e009c4b0eba7e5648a483832fc32ffe9c9e1b5441fbf2a6b7`  
		Last Modified: Tue, 02 Jun 2026 10:20:59 GMT  
		Size: 6.3 MB (6263754 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16b932359fbe4c3da2cfbd9cba22e64540394fc0a424fd6c895f9c991efbcabb`  
		Last Modified: Tue, 02 Jun 2026 10:20:58 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
