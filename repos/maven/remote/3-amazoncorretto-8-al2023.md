## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:9e7d8f4fc63e84c4ea6e1d63b501fe281999f3fbd06ef53d4408075fb0ac9c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4b22fbeb21e4b82355a25d919b838ba58feeb24734bd61a111956ccaf2d0575f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.6 MB (387552178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda402547ed38cae6b4eaccf0cd4bdb2bdfa2be4ea98027eb282558de5bbebd7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:19:49 GMT
ARG version=1.8.0_402.b08-1
# Fri, 05 Apr 2024 19:20:25 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 19:20:27 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 19:20:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:980f715748e4bf5e448b2d8a60d420f10ff6f8ba02cec072a8c1fa17f5f81dfd`  
		Last Modified: Fri, 05 Apr 2024 19:36:17 GMT  
		Size: 278.3 MB (278313764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6a89a5be1ef331d96b8d99105899b25653514f358cfb8f31610158a70713d8c`  
		Last Modified: Fri, 05 Apr 2024 20:59:46 GMT  
		Size: 47.4 MB (47433194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2c3d2cc2838e6b34b3e94811e15ddbd02b6e1b99b3fa317ebdf4d55a9848de`  
		Last Modified: Fri, 05 Apr 2024 20:59:45 GMT  
		Size: 9.5 MB (9479935 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f186ca6b23dfee5ed869eccb8118ec49d628caf9b9b9535441be4469496f4c53`  
		Last Modified: Fri, 05 Apr 2024 20:59:43 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afb2af3e149b94ecb44f476c8a71113bc2708e3cd51fd15b466c1d284120362f`  
		Last Modified: Fri, 05 Apr 2024 20:59:44 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2d6827bdaaf9b9b14753da6460336438281dfa74d0be351ab781dae7076e26b`  
		Last Modified: Fri, 05 Apr 2024 20:59:43 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:47c38b75f69acba0eff57ed380ed41b44961817c9562624ab307b304d5a2ec1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.1 MB (225068912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9a136ab304b5b206aa2d8572c3ea3637a2e2e4464140e8b435ae5903dbf82d6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:43:34 GMT
ARG version=1.8.0_402.b08-1
# Fri, 05 Apr 2024 18:43:52 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 18:43:53 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:43:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b8230ce60e9682f3662e8258ff1ee19f75ec7d58f5117994164b95327549146`  
		Last Modified: Fri, 05 Apr 2024 18:55:45 GMT  
		Size: 118.5 MB (118549025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c929a0eb6fa520bc12e546eb5d31e64c3fd00ef2a72f6610e2f24aae5eda5bbc`  
		Last Modified: Fri, 05 Apr 2024 19:42:07 GMT  
		Size: 45.6 MB (45630242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dfc8a64020f0d5c13a70041f5199ee65124b07b8760ee7fc82a986c0752d30e`  
		Last Modified: Fri, 05 Apr 2024 19:42:05 GMT  
		Size: 9.5 MB (9479940 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1124537bca98933cc65ce231192d39312d15dfaf8ff4223afa57d0e7fb6b6223`  
		Last Modified: Fri, 05 Apr 2024 19:42:04 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d8aa68e45a99abfbc4105e8d215f98f3b442048b3a9b33ce47eafff044ce00e`  
		Last Modified: Fri, 05 Apr 2024 19:42:04 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e27cfa173b771ec142407e24b4ef50f95cdeb64ffc998c72951ea092e6b3a497`  
		Last Modified: Fri, 05 Apr 2024 19:42:04 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
