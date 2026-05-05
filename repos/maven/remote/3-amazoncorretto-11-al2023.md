## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:e53570c5ca8b6bd0f9dacf7e2e985480d04a0d477868d68262275c8e9fdef968
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4e3939497ee430ac8c6ba771b42a9823443f8da8c2fc2a40ea13eac4570120ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.2 MB (344194020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27dbdade279ebbbcebd5c2b8356f2045c7817361428a1585fd1025e9d402b12c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:45 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:45 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:45 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 04 May 2026 20:44:12 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 04 May 2026 20:44:15 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 04 May 2026 20:44:15 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:44:15 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:15 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:15 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:44:15 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:44:15 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:44:15 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:44:15 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:44:15 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:44:15 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:44:15 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:44:15 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177f5f6694b7a14aaccd527d192e8e76c94dfecbb9fdd2f8693b660e84198ec2`  
		Last Modified: Mon, 04 May 2026 20:12:07 GMT  
		Size: 153.5 MB (153472514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843a1eeccc98155c7f718e6d743b53f3de1a11c636b8cf89a347cbb7475343f1`  
		Last Modified: Mon, 04 May 2026 20:44:35 GMT  
		Size: 114.3 MB (114301566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a193db242b5be48700622c54169e27b95b500c72659784b2a7a6b2a7b91bdb`  
		Last Modified: Mon, 04 May 2026 20:44:31 GMT  
		Size: 12.5 MB (12529956 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61609de0b6d0d151199206775a0f8a11ef70bf5e487da9c56f69a72c3527ee0f`  
		Last Modified: Mon, 04 May 2026 20:44:31 GMT  
		Size: 9.3 MB (9312220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c3b928f2499c88f123c865695a4abe8cc305e1cc322dbecc33cb0cb94a3d30`  
		Last Modified: Mon, 04 May 2026 20:44:31 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d3e596beb34aad398493db4f818383a1d2a28ee7c514f8e47604c6b28ae037`  
		Last Modified: Mon, 04 May 2026 20:44:32 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:87d846a7303d35212e39da1539f140a265b16a80013b412b892a5f5de27d4a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3872e853b59869a518609996cc0e36570dfda74ca79901aea8c8a17acf0c7f7b`

```dockerfile
```

-	Layers:
	-	`sha256:671b158b7e28c79ca29c83a160b18187e679cb10dcf39f161c4c87e6bcf71abb`  
		Last Modified: Mon, 04 May 2026 20:44:31 GMT  
		Size: 6.3 MB (6263977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dedcbc30a5d6dfca2f539b00608f06e9f311fd746d36cf254d9c7f7cf82a0f84`  
		Last Modified: Mon, 04 May 2026 20:44:31 GMT  
		Size: 16.3 KB (16288 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:03384918e4a6e7829036f89f33aa112b588105f2f7c40038009e0ca478aced8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.7 MB (340672353 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:046ae131494e28497393430044a56afbb2966f32a7b77bf50d6ff4f16a95a11a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:32 GMT
ARG version=11.0.31.11-1
# Mon, 04 May 2026 20:11:32 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:32 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Mon, 04 May 2026 20:44:19 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 04 May 2026 20:44:22 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 04 May 2026 20:44:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:44:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:44:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:44:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:44:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:44:22 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:44:22 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:44:22 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:44:22 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:44:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:44:22 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:838136ec5b6ab2b88d9936cfc6ef1491350d124ec8e540cec804c91561010d10`  
		Last Modified: Mon, 04 May 2026 20:11:53 GMT  
		Size: 152.1 MB (152051592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c34678777f318f8b48f42950d2af394849744d4aad61d795362c57f2bb5bafef`  
		Last Modified: Mon, 04 May 2026 20:44:42 GMT  
		Size: 113.1 MB (113056624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f943d3cc32fd6f6940dd25487f7f93dd70bd280d9fea49e63aa5a870441bdc82`  
		Last Modified: Mon, 04 May 2026 20:44:39 GMT  
		Size: 12.8 MB (12794106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf30e0e7b450516f665de793491b32981cd648df29a09cb5e82272d7f97f6a`  
		Last Modified: Mon, 04 May 2026 20:44:39 GMT  
		Size: 9.3 MB (9312250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc43366cf5de5bfe3be7710c293c14724d2b772f36ef1db45bb8e2031330c90`  
		Last Modified: Mon, 04 May 2026 20:44:39 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3298e59fa21ad402684964f69969c93fad64a0265b3ea6800c2e0e59fe48399`  
		Last Modified: Mon, 04 May 2026 20:44:40 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:bbbee9f029c9b0b3dcb2f80652a60ed88aee6c99484b990abdd050fc2d8cb676
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6280187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae09796d755273718e18d1aa44e32304b3cc894bbb84cd1961f7147542edb5d`

```dockerfile
```

-	Layers:
	-	`sha256:a7228eb8f7522188abfb353c68d8af9ab410e7de8455b888e3e3594068b760e6`  
		Last Modified: Mon, 04 May 2026 20:44:39 GMT  
		Size: 6.3 MB (6263751 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b393b646535af11032e33a785e71590fe611e5a4c4dd2a1e591875444f7307c`  
		Last Modified: Mon, 04 May 2026 20:44:38 GMT  
		Size: 16.4 KB (16436 bytes)  
		MIME: application/vnd.in-toto+json
