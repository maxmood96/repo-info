## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:e88eee7d9e085baf9bbc6d581e9d5032a2ce281b7d909913624875cb2f67fee5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:88842e2d4bbaa6d08b1b8678ea22cca8d15d6842285149f0805e9b26e817d069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.7 MB (266678604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1e9b368ba60555e9dcf08bec317b0671cdf697d5efa6630ee811851ef0ee907`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=11.0.24.8-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:762416386eec43a42d13844d5d37a76fdbfda9af554f0cf91313579d8394a14f`  
		Last Modified: Thu, 25 Jul 2024 21:02:30 GMT  
		Size: 153.8 MB (153792445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:759a81ad41d24e4641c5664247c0ecbcb518db27f8a97bdb69cf950d85062f06`  
		Last Modified: Thu, 25 Jul 2024 22:00:47 GMT  
		Size: 51.4 MB (51409135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a7f4e7ef5c3e09c4fb31f2c4230d2b52365076e39acc587c9ee2baf0f086beb`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 9.2 MB (9161804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e9793f5e965dc6a0d01818dd5ce5bd33a35f0dce576a19e39ddf784eed6d40d`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91b49b56fd217049f9465289f1dcbb1710a0fdede2b138d06bec4c4442e0f34`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:3e50f14139e13bdf05a2eb1d1db268cabaf1b822a125bc5d7a94f0953b60bb62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5509919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e8da7a3fc9a6213966cdd51e090640e15eb5fafa7661b4b0884ce3ba7d4951`

```dockerfile
```

-	Layers:
	-	`sha256:d78592fdad24d508d1e51de7bc91592b95905ff2385e0fa7627679404c8e25f4`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 5.5 MB (5493543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85a5d8c25c85764e43495b2e36de28170168dd111770e2197ecbb56f87ff8822`  
		Last Modified: Thu, 25 Jul 2024 22:00:46 GMT  
		Size: 16.4 KB (16376 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:9320a13ec30d41420384473df626ec3ff45a70a0acfeb69b536809ef4aaee021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.9 MB (263933015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1194615ef9f8fded713bf2aefa90e7f446676d1f371e4af45ef07e006e60179f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=11.0.24.8-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
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
	-	`sha256:69f1520adb0e35dcf91717c80b7867ab26fcf8ef8506b9831fcca72a1b38b618`  
		Last Modified: Tue, 23 Jul 2024 01:08:54 GMT  
		Size: 51.4 MB (51402016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93ca82809d6f0e47a5b8ca261f87fc0b700b592936cda77d6936afc9c917213`  
		Last Modified: Fri, 26 Jul 2024 01:50:40 GMT  
		Size: 152.2 MB (152246323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230fcad61cb8ba8782aaeb9979b0bcfce6d5876e9762e73f4e961c56605d0d33`  
		Last Modified: Fri, 26 Jul 2024 03:02:08 GMT  
		Size: 51.1 MB (51121856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1cf346d2d991bc1710a316a8956176d50f6183392db5e95561551cf821a6f0e`  
		Last Modified: Fri, 26 Jul 2024 03:02:06 GMT  
		Size: 9.2 MB (9161776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8126e5be138295031c8c8077b55f03ba7485a8c624262f56c10397ba45c44183`  
		Last Modified: Fri, 26 Jul 2024 03:02:06 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f977d84f143ed955a5730199fce0d70a6e710d203c81fa807cf9bdf89d2a23f`  
		Last Modified: Fri, 26 Jul 2024 03:02:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8db2acee5a73daca753acd8ff63175a6e27cf1aa3c230d77e445e8af49386171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5510417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f639c04949247e6272fcd6f23425f1762d8878fde848e12abfbfb4d4aacdd19`

```dockerfile
```

-	Layers:
	-	`sha256:958b53b8a3c2556b6e608698d99b254e6590406067dcd8868a684dcf367d1476`  
		Last Modified: Fri, 26 Jul 2024 03:02:06 GMT  
		Size: 5.5 MB (5493316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e135e8d5f3cb6c5a1ecf95691bbfe1a622ae5ac6c627415e8d7ab3217fc5da`  
		Last Modified: Fri, 26 Jul 2024 03:02:05 GMT  
		Size: 17.1 KB (17101 bytes)  
		MIME: application/vnd.in-toto+json
