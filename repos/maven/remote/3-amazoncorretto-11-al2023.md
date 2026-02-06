## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:6b8b2d89a92da8fcf986ada0a9e15b04c4c594a64cb8b84905ef0e7dba41d739
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4394e74ef1a12a43b259f39d89833fbf9a005aabb8bf20ad1a7d07ea19f3faf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328995475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26a3c8e3e3048e97fe470f994bca95f611efd4cbb8762f15be41295d99127c6b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:06:57 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:06:57 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:06:57 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:06:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 05 Feb 2026 23:29:35 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 05 Feb 2026 23:29:37 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 05 Feb 2026 23:29:37 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:29:37 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:37 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:29:37 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:29:37 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:29:37 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:29:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:29:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:29:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:29:38 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:29:38 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:29:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:29:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:29:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:402caadba9faf237352f0a6218ffdc967bda733b1529ca888757943968898ade`  
		Last Modified: Wed, 28 Jan 2026 04:07:18 GMT  
		Size: 153.4 MB (153366942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e56a73b7660f2bcabeaa85995ea0e4ff4226cc63f11a51da0c6b6dd6f62bd39`  
		Last Modified: Thu, 05 Feb 2026 23:29:57 GMT  
		Size: 99.8 MB (99790582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b12332df052985f17d10e65a18efe1f2a16146870703ae11c8a074329cc31888`  
		Last Modified: Thu, 05 Feb 2026 23:29:54 GMT  
		Size: 12.5 MB (12500837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:754ceb6966495badb31db656e87d7d2800207ba3bc6a560c8840b9e135c6a43e`  
		Last Modified: Thu, 05 Feb 2026 23:29:54 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e63ac0d974dbf6bc6b343dff82b16a141a47a6b9640cd90327a6ea28032d66`  
		Last Modified: Thu, 05 Feb 2026 23:29:54 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78236e6e52dd01c9d2d79949dfa565c758d27bab8fa23646c220fe4d8c9504c8`  
		Last Modified: Thu, 05 Feb 2026 23:29:55 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:4bfa2344ba8e344e4cb0729e0c8da113c33e46b2731f993f74f75ca20563aaf4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e195af020961cef7823326d7db5275af7451c7d860e98f961fa09bb9de108f0`

```dockerfile
```

-	Layers:
	-	`sha256:f450de07a0c6d1f8a1f44d4b00784b04e8aa8d5bd1da615e501220d7383bba41`  
		Last Modified: Thu, 05 Feb 2026 23:29:54 GMT  
		Size: 6.3 MB (6257535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bb81604dab4689587be6f543724cb4bb4dd1e2a57589729bc5fb3f52aa8580b`  
		Last Modified: Thu, 05 Feb 2026 23:29:54 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2c0bc399654a3c87a4f1444f511414c2b43065fd84e2fe6d9a04eac3c29c03e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325713381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc85494df59e662850e0baf2e9cf156f9624329fef4c595ff1a3ccd2d1d7edf7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:27:23 GMT
ARG version=11.0.30.7-1
# Wed, 28 Jan 2026 04:27:23 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:27:23 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:27:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Thu, 05 Feb 2026 23:40:31 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 05 Feb 2026 23:40:34 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 05 Feb 2026 23:40:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:40:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:40:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:40:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:40:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:40:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:40:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:40:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:40:34 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:40:34 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:40:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:40:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:40:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e130b48db658a3d47222a6ded8a1fec4b2b4ea85450905bcd926798478f901`  
		Last Modified: Wed, 28 Jan 2026 04:27:44 GMT  
		Size: 151.9 MB (151921736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c7bef952795f195263bddcadaa346b4d396da064ea73442236b255ae0ef99a0`  
		Last Modified: Thu, 05 Feb 2026 23:40:53 GMT  
		Size: 98.8 MB (98797538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76fdf193fb215c4f3980a937bc545bd59b45511ce58b0a7c7279a3af4210c21e`  
		Last Modified: Thu, 05 Feb 2026 23:40:51 GMT  
		Size: 12.8 MB (12764195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33a979ae67a7993b50981b545b04af65a394f59117abfd343b93a8f0fdfda779`  
		Last Modified: Thu, 05 Feb 2026 23:40:51 GMT  
		Size: 9.3 MB (9312232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:648b1f6129c70a1e553d4afb53df9ecaa27da99ae76174c5b3ece0bf6ca9fe36`  
		Last Modified: Thu, 05 Feb 2026 23:40:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53132236f17da7461f44c2817935399c9745af864cf0345d531c65330256eba6`  
		Last Modified: Thu, 05 Feb 2026 23:40:51 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ce659752fcd8558e630d1f219b20a198356720dc7d4041e58393d3c2fa85b0a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2a82b58e23c4bfafa290753e7a34be4ffa8da3cd32dc3b36639a92858b8d291`

```dockerfile
```

-	Layers:
	-	`sha256:69156d54c686f3056e9b55a2a1be2db1dc4f83c709a496c1afd675486f90e1e7`  
		Last Modified: Thu, 05 Feb 2026 23:40:50 GMT  
		Size: 6.3 MB (6257309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe16c1d6ef7bc16bc7b6a435391e38aa0290a78dd8a3313d293fc824fad03a66`  
		Last Modified: Thu, 05 Feb 2026 23:40:50 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
