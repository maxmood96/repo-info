## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:9902b8fbcd55e33f025d91a4608a0b5f66602b596aa5d411f2d78fcee02d7db4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:52c94ec70d69805ad9e0e8f0d0f44410ed4079825eebdf6dc92f0617f6611041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.3 MB (268317346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03252a53d58d8460b7d4cd16b4cfb03e12a58ea76ee1779a860f9ec0ce089e50`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:1a64694c076f4e5a1aad0a3ea24080e6520840f532ade5fd6b4f5f6a7cd949b9 in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=17.0.11.9-1
# Mon, 27 May 2024 15:57:48 GMT
ARG package_version=1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:25f617ca51f740a5a4c48d42acec404063181c588237158652d8a28cdd8abea7`  
		Last Modified: Tue, 11 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad4003963fa286260f1699ae024d3e24a52c460ec3f38df6f4b124575f96a7a1`  
		Last Modified: Thu, 20 Jun 2024 18:21:49 GMT  
		Size: 157.0 MB (157044084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df854b53ae1d095ec08435b11ffac68cf9028f3dedc56b58cabbca7a035d61cf`  
		Last Modified: Fri, 21 Jun 2024 02:01:35 GMT  
		Size: 49.3 MB (49305116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05ea1a385d5dc76d19fedc98934d94a3d59b86c35b601d3cf7453e475f04263`  
		Last Modified: Fri, 21 Jun 2024 02:01:35 GMT  
		Size: 9.6 MB (9647588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:075aa95ea7944445c9ba41117eceab1bdea9496ab006d42edfb24283ec7c01ae`  
		Last Modified: Fri, 21 Jun 2024 02:01:35 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ffb951f88c50d72332cc878e42a05e8c0ff116fede1bd69ff794311747f4bda`  
		Last Modified: Fri, 21 Jun 2024 02:01:36 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8372ac589f9dca209c85a6ff487efbcd166fd97367927762882a2cb5c41ddb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ba7fc21ae81ad6e4cd7bd57c36815032bceb5325886c5ec5ee5b7574b065eff`

```dockerfile
```

-	Layers:
	-	`sha256:8c57e90868f39f71096e2f0a024cd9a1709befa7bf48589b123e21f0faab837c`  
		Last Modified: Fri, 21 Jun 2024 02:01:35 GMT  
		Size: 5.4 MB (5432562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6832c5878e230c767e004860f3fdd6316ba449a607a4b9cd3d5a61d811987f1`  
		Last Modified: Fri, 21 Jun 2024 02:01:34 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8c1cda01a37dc370950ddb9d998d52d4225aea9f8a9392786d46a785522e39d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.1 MB (265082776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:817fdf53530e6772c4d6dfa0b167ef1a563c3807de3340e9a786131beeea6ab1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 27 May 2024 15:57:48 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Mon, 27 May 2024 15:57:48 GMT
CMD ["/bin/bash"]
# Mon, 27 May 2024 15:57:48 GMT
ARG version=17.0.11.9-1
# Mon, 27 May 2024 15:57:48 GMT
ARG package_version=1
# Mon, 27 May 2024 15:57:48 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 27 May 2024 15:57:48 GMT
ENV LANG=C.UTF-8
# Mon, 27 May 2024 15:57:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 27 May 2024 15:57:48 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 27 May 2024 15:57:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 27 May 2024 15:57:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 27 May 2024 15:57:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 27 May 2024 15:57:48 GMT
ARG MAVEN_VERSION=3.9.7
# Mon, 27 May 2024 15:57:48 GMT
ARG USER_HOME_DIR=/root
# Mon, 27 May 2024 15:57:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 27 May 2024 15:57:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 27 May 2024 15:57:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d3f08dfec1b60aa193195b32e09bbde055cc300cf866d64fb9cc03885074e4`  
		Last Modified: Wed, 05 Jun 2024 02:44:12 GMT  
		Size: 155.7 MB (155744539 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db236d4d076f98de8234bc7df030f3590e763640be18f06115305584a7a276c2`  
		Last Modified: Fri, 21 Jun 2024 16:56:07 GMT  
		Size: 48.3 MB (48285693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19180e6f027a94135bc9039e275cd9db54df18026eeddb2123a4f30524757fd6`  
		Last Modified: Fri, 21 Jun 2024 16:56:06 GMT  
		Size: 9.6 MB (9647619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe0f41a3bacd37f7444e541e827cf73a9c866db13cd3ecfef609e26446832416`  
		Last Modified: Fri, 21 Jun 2024 16:56:07 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d70fe075453169150a9a94b739a4ce3458fdadc0b1d6ae42d0a82bae9531f24`  
		Last Modified: Fri, 21 Jun 2024 16:56:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:dda3644afb700ec7fb5ac444aedb410801e4174e5c4a0b5010625596c832e479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5447183 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d867dd435c222a1be28545009d4f45e2756aea1b13ba2ee740d8d841c6a6afc`

```dockerfile
```

-	Layers:
	-	`sha256:1a015c95abdf2dc860c4abb1dd0b7cf8028a3dd2fe025b0e1fad405d5dc4fc30`  
		Last Modified: Fri, 21 Jun 2024 16:56:05 GMT  
		Size: 5.4 MB (5430269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b2414bac668cf20dd790037fb6b31eac3d104d64f676e5a74f558f2c2419424`  
		Last Modified: Fri, 21 Jun 2024 16:56:05 GMT  
		Size: 16.9 KB (16914 bytes)  
		MIME: application/vnd.in-toto+json
