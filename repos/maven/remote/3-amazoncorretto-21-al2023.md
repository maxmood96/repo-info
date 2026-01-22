## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:9b0cd45e655aea19b93cd0d992eebdd094b56a79b2e80b25b68fb9264ee079ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2a59914574019302d7336eabd35cee8365c9909135f4da86e23fb5e2edb957b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **345.2 MB (345154882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd8ac4f85d0619673ef86d5365508c8b4004b2863506352a73bfecc741a5f7e3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:17 GMT
ARG version=21.0.10.7-1
# Wed, 21 Jan 2026 19:01:17 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:01:17 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:01:17 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 21 Jan 2026 19:17:01 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 21 Jan 2026 19:17:04 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:17:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:17:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:17:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:17:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:17:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:17:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:17:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:17:04 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:17:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:17:04 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:17:04 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:17:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:17:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:17:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:08:12 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d21ced9c39d50d5e7b3415e5936b9fc06cefc74e724f65fb81d292bb3701567`  
		Last Modified: Wed, 21 Jan 2026 19:01:41 GMT  
		Size: 170.2 MB (170196420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6d26baee2b4ae570840bedc939b3889a541e1fd892ff3fb95a05f5d83b8d7d`  
		Last Modified: Wed, 21 Jan 2026 19:17:23 GMT  
		Size: 99.1 MB (99126600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c1189d0f08325fe449b592886ec554dc40be331dc2107c8ed7a6b581614e2f9`  
		Last Modified: Wed, 21 Jan 2026 19:17:21 GMT  
		Size: 12.5 MB (12497378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dce87640e661cf9d3823d24aa82104c5ec40fd731a8f13f6cd486f4194c1e381`  
		Last Modified: Wed, 21 Jan 2026 19:17:22 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06033ca1e09b438e586c85c0559d4688c0128f6b42c5ed4f18be54817f40e47f`  
		Last Modified: Wed, 21 Jan 2026 19:17:21 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc11dd5d7bf211fac6571ea14e5293d53ef4fda56fa44bf455a20cb2694b5fbf`  
		Last Modified: Wed, 21 Jan 2026 19:17:22 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:0ef6479ccaec98653767f52e112626d8ab15a71f926bd2ef853a67efd4e4ede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95589632f24e27c93836ab7b0adba94eb1cbd3992148d9d7d5f76b2e6e91af4b`

```dockerfile
```

-	Layers:
	-	`sha256:b0dff65c0cc90837aca1d108285ee9414a836d3b25aa6eb3e7cefe9c2e07d9c6`  
		Last Modified: Wed, 21 Jan 2026 19:17:21 GMT  
		Size: 6.2 MB (6234451 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52f103a84340ca1212fa70610ab08421dd7de779e860705afe509fab8737a4d7`  
		Last Modified: Wed, 21 Jan 2026 19:17:21 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b2f62973cf3d22bf7066545237ef19166acbd1dc22313888137fe493378e5b80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **341.3 MB (341336197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9c2b3c37485ba49c20ef1f0e14948e4402a89dda731ac63891352876cd1f27`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:15 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:15 GMT
CMD ["/bin/bash"]
# Wed, 21 Jan 2026 19:01:27 GMT
ARG version=21.0.10.7-1
# Wed, 21 Jan 2026 19:01:27 GMT
ARG package_version=1
# Wed, 21 Jan 2026 19:01:27 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 21 Jan 2026 19:01:27 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:01:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Wed, 21 Jan 2026 19:21:57 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 21 Jan 2026 19:22:00 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 21 Jan 2026 19:22:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 21 Jan 2026 19:22:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:22:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 21 Jan 2026 19:22:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 21 Jan 2026 19:22:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 21 Jan 2026 19:22:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 21 Jan 2026 19:22:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 21 Jan 2026 19:22:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 21 Jan 2026 19:22:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 21 Jan 2026 19:22:00 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 21 Jan 2026 19:22:00 GMT
ARG USER_HOME_DIR=/root
# Wed, 21 Jan 2026 19:22:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 21 Jan 2026 19:22:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 21 Jan 2026 19:22:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:60a6ef84e125e61efd6725688f23e752e71a4dd414aa447d2bc3e2a4a5f823e0`  
		Last Modified: Wed, 07 Jan 2026 22:47:25 GMT  
		Size: 52.9 MB (52914357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6671b25031554e09497753c844b250075e81cfc0bcb21c695d6cc03fe34a6452`  
		Last Modified: Wed, 21 Jan 2026 19:01:52 GMT  
		Size: 168.5 MB (168468252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:542518ceb0bc516d598b648d3e7f6bcf599d8684fab008a0746910c1ce20b516`  
		Last Modified: Wed, 21 Jan 2026 19:22:18 GMT  
		Size: 97.9 MB (97884159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be799d904aae40d692954a52715d47fc1ae49217dbf7ebf21dad4e6c283e7006`  
		Last Modified: Wed, 21 Jan 2026 19:22:16 GMT  
		Size: 12.8 MB (12756136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20a05914e3511e778ea3381ad55962e9be6d47bea350297b503c78225cb0d055`  
		Last Modified: Wed, 21 Jan 2026 19:22:16 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91bb6a7e7d5ea656b26508d53290d97f3bf39d66bd632d7182f431699629b319`  
		Last Modified: Wed, 21 Jan 2026 19:22:16 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa24535990d1e7f34ae8ea2804b075e25782835161493086a3dd181ebeafe4a3`  
		Last Modified: Wed, 21 Jan 2026 19:22:17 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8100b3e9a98f065a2cfa20a8c758a9d9f35b3e5e2bb74f8d45a689f55cd40d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e341a9fbdc8de7c009a774d8bf717052f1fd8176913bfbd8dcdcf231264dc53`

```dockerfile
```

-	Layers:
	-	`sha256:bdb8253f8a9e52a49c5c8a389e791e2ab84d70e7ba90afe3bef1f0af6a1323ff`  
		Last Modified: Wed, 21 Jan 2026 19:22:16 GMT  
		Size: 6.2 MB (6233384 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0d4f059e8c5b80bcca25180503e0e525a5ce9f3e7501f9bcba90417c7aec3d`  
		Last Modified: Wed, 21 Jan 2026 19:22:15 GMT  
		Size: 18.4 KB (18432 bytes)  
		MIME: application/vnd.in-toto+json
