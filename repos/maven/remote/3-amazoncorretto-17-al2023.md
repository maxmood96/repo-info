## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:bd38b8c105209349447bbaf4db8aad6be50dba1baa2879e60cdb9cbec4e62558
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:b184070483fdd7603bd0958824bccf96e2413124f66f20535e0cf984112d387b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **270.0 MB (269985894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42785861593a905c7b887e8d91e17c001d264adc87ca6223d1627eb2fe6b3a46`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.12.7-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89bd119ee079341b2c2ea9b23787e6a4a8347634bf5ab7190338deec1e76acde`  
		Last Modified: Thu, 25 Jul 2024 21:02:36 GMT  
		Size: 157.1 MB (157101148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea23c881596a1a6830999d90e8f0c101948bfbdbc5264100be1e0b7627f7101`  
		Last Modified: Thu, 25 Jul 2024 22:00:49 GMT  
		Size: 51.4 MB (51407715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30f7ea9aedd6651ca2d5a01039ef489c26e6257e75f974703748e803b1d3c29`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 9.2 MB (9161813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e769d27134e66dd19a2afe33c70317bd0b853eff2c937295b93f24bd1e4a78d`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:088d652d5fc85b79490b9d12460c5cfbf5368358130fd50a712dce2dac8ffc44`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:aa3e216025942591dde5a28dd88578c7e5b7693d1de726694518be7e518fe076
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5483549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1f55eff7af1dcf050c4873937008b55bfe1269469af2a6903cbe03173106c9`

```dockerfile
```

-	Layers:
	-	`sha256:4d1397ed11d6e7cdb898fe3847a466e39a07573ae01a31e13e0de140f6ac1901`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 5.5 MB (5467174 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9de785742273b0974a1cb6ebf86c3c367cb599526963781524594647074bfa47`  
		Last Modified: Thu, 25 Jul 2024 22:00:48 GMT  
		Size: 16.4 KB (16375 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:821e67274d5c2caffd5a8c0486c4b28b465e77eaddf126c1063469aa01ad8490
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.2 MB (266245140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93b3afc182f6fe15b1f97df6f9581dc579a6915a5578dded28d0912dc6d02988`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.12.7-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ec1b57f4046e02cf6f4752cadcceed33faf19d4b8b4eef864c5a2515008ab5`  
		Last Modified: Thu, 18 Jul 2024 01:11:12 GMT  
		Size: 155.8 MB (155801066 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5cae7a50463cc0a343041b68142963455b9fb54732b1d92a405938c976e681`  
		Last Modified: Thu, 18 Jul 2024 02:10:33 GMT  
		Size: 49.9 MB (49880110 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e67b0caecb3772f493a512907e230fbb89bd55ab11b06ecd9678c3b437ea1c8`  
		Last Modified: Thu, 18 Jul 2024 02:10:32 GMT  
		Size: 9.2 MB (9161783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45e2ded9db29c2fb1e85bfb400bfeabba16dc863d27b6e79c1796107aecafb1`  
		Last Modified: Thu, 18 Jul 2024 02:10:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd6e919456d296f58f22ef415cf4f52d1dae04c6f8191c1a65ab5bd0475bad33`  
		Last Modified: Thu, 18 Jul 2024 02:10:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:f2acb6c8e6dd33beb17a0627ece85c8a690fa70e79ff38c0348eabab02cb0268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5483236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a433becf4c927e7a32d69db4b78e7c94e442c733e9b91c8034274e761a1413b`

```dockerfile
```

-	Layers:
	-	`sha256:7c532b82f0b7f6d1d57c38ac42704b720031775a35124aa012acd5c31010d425`  
		Last Modified: Thu, 18 Jul 2024 02:10:32 GMT  
		Size: 5.5 MB (5466101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3fc45b35811ba8477b219880d7e3f7855ceeff9455cba7e2819eabec243bd1f`  
		Last Modified: Thu, 18 Jul 2024 02:10:31 GMT  
		Size: 17.1 KB (17135 bytes)  
		MIME: application/vnd.in-toto+json
