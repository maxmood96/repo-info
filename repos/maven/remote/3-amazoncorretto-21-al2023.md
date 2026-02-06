## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:3c2f987dbf15d07ad42ce08d39e99c83629b84a47f9c8d2ba4c0724be7fc165e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:fe91485b3eefd67786202d6e7bf708ac995b3b1bf7079473d07c38e7729ae86e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.8 MB (345819283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603960a7ac472e72e7a0d58b7ef2ba6322d9873cb700e07c3f6b95708ba3703c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:13:29 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:13:29 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:09:01 GMT
ARG version=21.0.10.7-1
# Wed, 28 Jan 2026 04:09:01 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:09:01 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:09:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:09:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 05 Feb 2026 23:30:17 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 05 Feb 2026 23:30:19 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 05 Feb 2026 23:30:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:30:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:30:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:30:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:30:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:30:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:30:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:30:20 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:30:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:30:20 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:30:20 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:30:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:30:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:30:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4139f539d4e9c2d034d745f5d11bef856e6b733e375190b0a418cd47e1980468`  
		Last Modified: Wed, 28 Jan 2026 04:09:23 GMT  
		Size: 170.2 MB (170196306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb186c0a9ad5eeb5793f00231153096c0e4eaf710e9bdf12d446cc0df3bfd7cb`  
		Last Modified: Thu, 05 Feb 2026 23:30:38 GMT  
		Size: 99.8 MB (99788398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6f7fa83737d918bb680b99a6faacb7487e67580d2ea720f6377c925488bb84b`  
		Last Modified: Thu, 05 Feb 2026 23:30:36 GMT  
		Size: 12.5 MB (12497461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08186685055af4faf6d2c7557e7cdc767c751f11f6f8536dcd35ba21de2eddc`  
		Last Modified: Thu, 05 Feb 2026 23:30:36 GMT  
		Size: 9.3 MB (9312239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f415f72179104326e95e37fd18e5bbeaf218b27373af891f71aa244c8ca963`  
		Last Modified: Thu, 05 Feb 2026 23:30:35 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0062443918f77921b447b529635e46843f7cef80ce338ee70de898eecb621f0c`  
		Last Modified: Thu, 05 Feb 2026 23:30:37 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:efaf0806150ee8592d3849f41cf84a3c449cb6fb10459582357433580d12592d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3bda4bcc24d8678e82e0a5a39afc8086c78c89b4e6539e2b2b321aa68474d4`

```dockerfile
```

-	Layers:
	-	`sha256:f7a8c36668e7f64f57a34b03815a692faea8f5cdee718665e3ede27a4e15d2a9`  
		Last Modified: Thu, 05 Feb 2026 23:30:35 GMT  
		Size: 6.2 MB (6234451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cf895bcb763e2e19a271548e40ff4de3d414dbd8f4dbe35dbe39f9aa0b1229d`  
		Last Modified: Thu, 05 Feb 2026 23:30:35 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:c268926c616e66747f7d68a1c1baf6af4adac31c7b2c027b975e17474603c52d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.3 MB (342251663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0772388a8c7e519202e8f9c861534d012f530a78c92989e959fa8339130061b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 28 Jan 2026 02:14:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 28 Jan 2026 02:14:02 GMT
CMD ["/bin/bash"]
# Wed, 28 Jan 2026 04:30:21 GMT
ARG version=21.0.10.7-1
# Wed, 28 Jan 2026 04:30:21 GMT
ARG package_version=1
# Wed, 28 Jan 2026 04:30:21 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 28 Jan 2026 04:30:21 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 04:30:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Thu, 05 Feb 2026 23:41:16 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 05 Feb 2026 23:41:19 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 05 Feb 2026 23:41:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 05 Feb 2026 23:41:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:41:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 05 Feb 2026 23:41:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 05 Feb 2026 23:41:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 05 Feb 2026 23:41:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 05 Feb 2026 23:41:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 05 Feb 2026 23:41:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 05 Feb 2026 23:41:19 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 05 Feb 2026 23:41:19 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 05 Feb 2026 23:41:19 GMT
ARG USER_HOME_DIR=/root
# Thu, 05 Feb 2026 23:41:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 05 Feb 2026 23:41:19 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 05 Feb 2026 23:41:19 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dab383397a3bae2ff9144daec67d762c1416fa3658fa3eea12c446ddba20e48`  
		Last Modified: Wed, 28 Jan 2026 04:30:45 GMT  
		Size: 168.5 MB (168468790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98a9b188cbc60573c383f8b60aef533cb2b32e5788f95236d0607e11bf730c57`  
		Last Modified: Thu, 05 Feb 2026 23:41:37 GMT  
		Size: 98.8 MB (98795627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9efaacfdad6c3a95239cec9bfc5facc3c0bdab46d01cecbe5390af89a46baf43`  
		Last Modified: Thu, 05 Feb 2026 23:41:35 GMT  
		Size: 12.8 MB (12757331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2ac48a9c6a57de26e393efbe9becc7c92116b62544e6f4f79c00924b8571c2`  
		Last Modified: Thu, 05 Feb 2026 23:41:35 GMT  
		Size: 9.3 MB (9312235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:259f2e7ebfe7d5efd3b171ff51ea433111bdf40dbc71269c26ebb5c10eec02ff`  
		Last Modified: Thu, 05 Feb 2026 23:41:34 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c585e5c864cd138f5a0a90b8ee33f7d3bbd367040ba87926c9006a7d521b557`  
		Last Modified: Thu, 05 Feb 2026 23:41:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d1cdd14f44825f6e7eb77bb27782b627913e41b8dc28900eca1d35d686ac3664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b402d29a3accf0c6a3b6032f3ae4108930ee3f386c9eac5c9972de3521797b`

```dockerfile
```

-	Layers:
	-	`sha256:a161b27a3df2edeebe1c5bd4894bb713e598baebbd230b4675a62e5790e18d4b`  
		Last Modified: Thu, 05 Feb 2026 23:41:35 GMT  
		Size: 6.2 MB (6233384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a9b1f2918c672fb432c505e6b9bd7e3214ba61b581abd394706d8dc30de1fba`  
		Last Modified: Thu, 05 Feb 2026 23:41:34 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json
