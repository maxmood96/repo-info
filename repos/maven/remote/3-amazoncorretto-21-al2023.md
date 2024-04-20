## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:8d653ed25358201bdb352ce0d24e4be2f1e34ddf372d3381d22876f9c483cfa1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2fc09a047a7a8b544e1a16eca66ff84937f4fccc69c67b8f833294c0b966ba01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **279.1 MB (279085103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1981f3a7fe6b4c644f729852cc8973591ae2d0b0e4370ab8fa0affeab2cd74`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:10 GMT
COPY dir:c7d5463abe17dfd3879bd12c94f31ebdaedb939167b5199c40650e35e379f334 in / 
# Fri, 19 Apr 2024 22:25:10 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 23:00:24 GMT
ARG version=21.0.3.9-1
# Fri, 19 Apr 2024 23:00:24 GMT
ARG package_version=1
# Fri, 19 Apr 2024 23:00:48 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 23:00:48 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 23:00:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6f59c9417334b7a9eb6449cc09a14d6738ae8afbfb25d681f2c27740e7d4856c`  
		Last Modified: Fri, 19 Apr 2024 22:25:53 GMT  
		Size: 52.3 MB (52323609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82edc30e223bf0e8886d730c53d6f1e28b769b1a5307a3721ddd593dda51df27`  
		Last Modified: Fri, 19 Apr 2024 23:12:33 GMT  
		Size: 170.7 MB (170666720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c41727d44f6c6d7201287c6d5991dcff9f1fb88e31d7d309e598be557c78b5`  
		Last Modified: Sat, 20 Apr 2024 00:24:17 GMT  
		Size: 46.6 MB (46613444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88eee057eb6cbb207c629f56ddfebefdef5b91f221b4aca9f3d2a4e30b1ce75d`  
		Last Modified: Sat, 20 Apr 2024 00:24:14 GMT  
		Size: 9.5 MB (9479947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3f8121b1231148dd3b23883a625234b5f629aa5df35f507b26b3febedc27b8`  
		Last Modified: Sat, 20 Apr 2024 00:24:14 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd4e778c55423e81b7fd754d663ee2996a8518a09ef008ff0e0878792061bd22`  
		Last Modified: Sat, 20 Apr 2024 00:24:14 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ad24f2f4737e81eadb440836584a0efb874125dc33f93dba908ed197aef88`  
		Last Modified: Sat, 20 Apr 2024 00:24:14 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d2e1ed72bf6f00f414c8035761a4aa42ad35f4a15502604ca627756f1bd05224
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.9 MB (275932419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11f2d6d048ccdb5b6c62dfffabf5424e89039ececffd9b8025fa13ee652965e3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:10:28 GMT
COPY dir:e8d306065b89c24e8d7ed76b1f4a499224cd18e3ec44dc6823b5d039220ebc19 in / 
# Fri, 19 Apr 2024 22:10:29 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:36:37 GMT
ARG version=21.0.3.9-1
# Fri, 19 Apr 2024 22:36:37 GMT
ARG package_version=1
# Fri, 19 Apr 2024 22:36:58 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:37:00 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:37:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 18 Dec 2023 19:11:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 18 Dec 2023 19:11:15 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 18 Dec 2023 19:11:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 18 Dec 2023 19:11:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 18 Dec 2023 19:11:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 18 Dec 2023 19:11:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fff0db406e493d5737bccd8db4b9460e6d6c5e6d45f62e14ae7cb208fcc984a`  
		Last Modified: Fri, 19 Apr 2024 22:11:04 GMT  
		Size: 51.4 MB (51413307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cbb07772ff9e16181e1ac28ed4b3773fb096ab86fd9f27c436b80f992bdae4`  
		Last Modified: Fri, 19 Apr 2024 22:46:59 GMT  
		Size: 168.8 MB (168805744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d6eaf573ec97425b27ce5aa9e0095f481d0a2b7e8d6385fa1818e228513742c`  
		Last Modified: Sat, 20 Apr 2024 00:14:42 GMT  
		Size: 46.2 MB (46232040 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00648d72c68ac3d52a1be42359f446dc6ce5b351ba6c05de9c0d114d0b8c053f`  
		Last Modified: Sat, 20 Apr 2024 00:14:40 GMT  
		Size: 9.5 MB (9479946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f103979f72f19489a59ee6fe367e5eb009ebff4b38fb9fb4640354ab10c66813`  
		Last Modified: Sat, 20 Apr 2024 00:14:40 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3540349560a17ebce8717e0fcb73c3288eee57396f45f6b2332bf71a00361afb`  
		Last Modified: Sat, 20 Apr 2024 00:14:40 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51fcf026060ac16140ab0d90b87943eef251b6a06be6165d12df6cd5a7551108`  
		Last Modified: Sat, 20 Apr 2024 00:14:40 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
