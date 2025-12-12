## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:80f411ee8dc37def5bb6808f3b2698d5fac5a16b6797ffc8fc1fbce2df71b49e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:97ed7a62d6d31ae1576cd3614dbcd73311059dfc292852c46afc56c705000faf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.9 MB (497850736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f0370b39eb1a5e1915b65562992db5401d27059702b5abcc55ccd904649dd5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:42 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:42 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:42 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 11 Dec 2025 22:23:40 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 11 Dec 2025 22:23:41 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 11 Dec 2025 22:23:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Dec 2025 22:23:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:23:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:23:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Dec 2025 22:23:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Dec 2025 22:23:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Dec 2025 22:23:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Dec 2025 22:23:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 11 Dec 2025 22:23:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Dec 2025 22:23:41 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 11 Dec 2025 22:23:41 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Dec 2025 22:23:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Dec 2025 22:23:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Dec 2025 22:23:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa5671e4c6388bab5eaf668041a81c0906c37489a66a044c651a8ef17681b4`  
		Last Modified: Thu, 11 Dec 2025 22:12:45 GMT  
		Size: 330.9 MB (330888100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:355158a2e9211c7c76022dd73ee687b8982d038acfb76897e64cc2b1a216305b`  
		Last Modified: Thu, 11 Dec 2025 22:24:37 GMT  
		Size: 98.3 MB (98312461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f067583632ae3f043e2b293bfe3dbea2556f52742e2a215ae84439e9289cb21`  
		Last Modified: Thu, 11 Dec 2025 22:24:22 GMT  
		Size: 5.4 MB (5418097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b19d994252d4c335df0726ab59f8b77d9e678173757bb17002b84ffc2223015`  
		Last Modified: Thu, 11 Dec 2025 22:24:23 GMT  
		Size: 9.2 MB (9242573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236904b94c9ffe093c30e3c11a45ab56e29a09d0f445210090da2e091ea0ceb8`  
		Last Modified: Thu, 11 Dec 2025 22:24:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9571ed2d2d6c1b9bbb1c7f381e84f60b88d79d7cbcbf20e2ecb7d42442957bcb`  
		Last Modified: Thu, 11 Dec 2025 22:24:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e15641ca35b942137049bea0a9f65817c61cb0d8a72a89c9e02e940597c1da5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9fbdde61b8fe20d6972dc37145575f597a3d1087c919a6d297c9cebc0c4b1b`

```dockerfile
```

-	Layers:
	-	`sha256:70d053a405a97c91b464e28f38368e2e0ab0b20bae00c2296a401eb7e45d8c12`  
		Last Modified: Fri, 12 Dec 2025 00:28:47 GMT  
		Size: 13.8 MB (13828213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03c9ce475c871939d29a517f172a947729cc75090959865f0a84b09c9757ec0f`  
		Last Modified: Fri, 12 Dec 2025 00:28:48 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:2e56cc3f5e6c1c3e4d88f43309029cd616941bd77b632857b9b0ecd61af4c303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287760056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc4fe198ea6230ac918e78be2efab0f185f92f067fad44f4707003e5fe9f69a2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:30 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:30 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:30 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Thu, 11 Dec 2025 22:23:26 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 11 Dec 2025 22:23:28 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 11 Dec 2025 22:23:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 11 Dec 2025 22:23:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:23:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 11 Dec 2025 22:23:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 11 Dec 2025 22:23:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 11 Dec 2025 22:23:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 11 Dec 2025 22:23:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 11 Dec 2025 22:23:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 11 Dec 2025 22:23:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 11 Dec 2025 22:23:28 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 11 Dec 2025 22:23:28 GMT
ARG USER_HOME_DIR=/root
# Thu, 11 Dec 2025 22:23:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 11 Dec 2025 22:23:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 11 Dec 2025 22:23:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c48e9835d76eae2b2c4e9d6c02f6408efc2e56451c92c8fa9e4c21b8dd8690`  
		Last Modified: Thu, 11 Dec 2025 22:12:13 GMT  
		Size: 117.9 MB (117927059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:456e1efd596afacebfaa24873b7599351d7ffb86fc457704de931e2ab827704c`  
		Last Modified: Thu, 11 Dec 2025 22:24:07 GMT  
		Size: 95.0 MB (94986207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd9e8561bb0ca4e6604086db064e9729a7485ce0ea12938cbcbe6bbec3094960`  
		Last Modified: Thu, 11 Dec 2025 22:23:54 GMT  
		Size: 12.7 MB (12729719 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3680ac5663b6ca06ce55f9fc0fe708db91efd75385539564ced952a67e7f05db`  
		Last Modified: Thu, 11 Dec 2025 22:23:54 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9326927e78210a6bd00ee6e0952458e25d346ef7c0fb8662d26dfb5654371925`  
		Last Modified: Thu, 11 Dec 2025 22:23:52 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d6248df57e6d50d77dd87acf33d580120cf6a31f00940deee37e3803690506`  
		Last Modified: Thu, 11 Dec 2025 22:23:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d845b5c0c96654bc85aca1bebaa8a3bacbda01fd29ce3644361cfa993fa19633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec046c9293c6e351c66cda189ee1b420408a0d2ce97de5c9aa167b8d4c22d1b`

```dockerfile
```

-	Layers:
	-	`sha256:d6670ab9020df0824e1c66f6561c3976a8b8cddb89b7fa8c557b8e7f890dc1f9`  
		Last Modified: Fri, 12 Dec 2025 00:29:02 GMT  
		Size: 6.6 MB (6609534 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b41d3fd4db222dbe7752733b7bbcf4e30b0461a26459b16a7663dfd6e1608d6f`  
		Last Modified: Fri, 12 Dec 2025 00:29:07 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json
