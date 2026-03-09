## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:157dc7ab53d671f74a16f732c660ee674b317cdec48ee01c6228b767676242f7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:13abeb8db6e67e5f3fe98b21f18642cd4b1459f227c3e567e3a64f38b14f9522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.6 MB (505609830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f1ba54c7469cf25a5a15f697fdabca89dffa5b986aa4fccf730f166f3ed442`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:01 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:01 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:09:26 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:09:26 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:09:26 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:09:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 09 Mar 2026 19:15:01 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 09 Mar 2026 19:15:02 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:15:02 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:15:02 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:02 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:15:02 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:15:02 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:15:02 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:15:02 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:15:02 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:15:02 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:15:02 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:15:02 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:15:02 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:15:02 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:15:02 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2584a8e504dfaf493eadaafafbabd8b97f7cb5bbe3cb6a319fb37cf3c4335d86`  
		Last Modified: Thu, 19 Feb 2026 02:57:43 GMT  
		Size: 54.0 MB (54032840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75b18538accb88a58aed84b71209400853929ec0f545d15034e35d003d55ec3`  
		Last Modified: Mon, 02 Mar 2026 23:10:21 GMT  
		Size: 330.9 MB (330924119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a05f2348b3e9cb5d08bebdb4d1b02555ca8abd424296c773cfd0e7ad301823`  
		Last Modified: Mon, 09 Mar 2026 19:15:33 GMT  
		Size: 105.5 MB (105496505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bae3105721029c428745ec8889c0d27efd87e3ba0f4e697bad6d836833153ec6`  
		Last Modified: Mon, 09 Mar 2026 19:15:30 GMT  
		Size: 5.5 MB (5457803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f80180f94464ea4d37d52380b693adf207727446b7640e19716f86348910471`  
		Last Modified: Mon, 09 Mar 2026 19:15:30 GMT  
		Size: 9.7 MB (9697521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f8da40c95cba08d6f4fb2d382353cc125d7d15f27cc933071199a058fe97945`  
		Last Modified: Mon, 09 Mar 2026 19:15:30 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af86cf51e760fcc77a1db3966d799998caa0c491e3f81fd0fb66cbfed5e04dac`  
		Last Modified: Mon, 09 Mar 2026 19:15:31 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:2524f77248afc9d907431514382c542dd7f3bca9e5e55e3154196586646eefca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13853049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:457507db0df94cdb9abaa98009c81d68297e5adcb8bf0e7d29ede5fc57a834ac`

```dockerfile
```

-	Layers:
	-	`sha256:1298cb2a5cf8e7f0574282b9b22c2f805586a7ea29905fb596ca070ddf59eb7d`  
		Last Modified: Mon, 09 Mar 2026 19:15:30 GMT  
		Size: 13.8 MB (13834767 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc19868c672644af634da3242e565ecaf94be71a823acd5e3dbc753f810843f7`  
		Last Modified: Mon, 09 Mar 2026 19:15:30 GMT  
		Size: 18.3 KB (18282 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fba4520f86aca87aa36da6157c4f97c788ca540121abf0563c059454aa5fd1ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **295.2 MB (295233738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4e0eec53a71129e0e71e5ebe894c9b2d64265edf69e9932a2e35eba7467868`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 02 Mar 2026 23:02:04 GMT
COPY /rootfs/ / # buildkit
# Mon, 02 Mar 2026 23:02:04 GMT
CMD ["/bin/bash"]
# Mon, 02 Mar 2026 23:09:57 GMT
ARG version=1.8.0_482.b08-1
# Mon, 02 Mar 2026 23:09:57 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 02 Mar 2026 23:09:57 GMT
ENV LANG=C.UTF-8
# Mon, 02 Mar 2026 23:09:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 09 Mar 2026 19:14:31 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 09 Mar 2026 19:14:34 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 09 Mar 2026 19:14:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 09 Mar 2026 19:14:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 09 Mar 2026 19:14:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 09 Mar 2026 19:14:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 09 Mar 2026 19:14:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 09 Mar 2026 19:14:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 09 Mar 2026 19:14:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 09 Mar 2026 19:14:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 09 Mar 2026 19:14:34 GMT
ARG MAVEN_VERSION=3.9.13
# Mon, 09 Mar 2026 19:14:34 GMT
ARG USER_HOME_DIR=/root
# Mon, 09 Mar 2026 19:14:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 09 Mar 2026 19:14:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 09 Mar 2026 19:14:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9330fae67a20d9aa2569828674140d8b67d50cfd127cb99ba0f9be275d35f976`  
		Last Modified: Thu, 19 Feb 2026 02:57:42 GMT  
		Size: 52.9 MB (52941319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de3d3a8cae532adff8f9f52c5b597c5da455126a70f8cfc9bb3ff95473ed1ac`  
		Last Modified: Mon, 02 Mar 2026 23:10:17 GMT  
		Size: 118.0 MB (117965736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b961c48558a8c8ff159b5c1cc18746093fbf0b842fa37eab1196ed1448fadcac`  
		Last Modified: Mon, 09 Mar 2026 19:14:53 GMT  
		Size: 101.9 MB (101850619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427a171343ce0296c5ae3e9d23283aca79f4f7360fe0c525b7740261efdc033e`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 12.8 MB (12777471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc3f52e6817e586e7d7a410fe73ae67bb997841d33605a28803a52b89fcae58`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 9.7 MB (9697552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c676edb5c6238362171416a5a3783576f69e0edc028749e2228c0e4ed4153df`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54530d08447d4f3a22eba0f215c7f30860bfd37a496600c6bc66c6dca6a93f73`  
		Last Modified: Mon, 09 Mar 2026 19:14:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:47d8a49ae5ab9ab9ac516e8982fd3c2c471b0a267b37a21fc0ec9fe5348542c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:facdd8f2718189ede052166aff138454b8437aa3a0eb8f532b0951d333906765`

```dockerfile
```

-	Layers:
	-	`sha256:f49044ac1d9d2ecd1eaad6b11225c8cdf1f95499cbfd8a45e9a34d60a56b12a1`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 6.6 MB (6616088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c48ff2d7d00cdf8fda860ef2cd6d07d80ed1d37e3f85245a9777e397dea0049e`  
		Last Modified: Mon, 09 Mar 2026 19:14:51 GMT  
		Size: 18.4 KB (18434 bytes)  
		MIME: application/vnd.in-toto+json
