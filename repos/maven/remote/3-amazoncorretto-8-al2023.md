## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:2fe9a3449143f95548a7cce2e965bbefee989177f2828258e376093a9f9516eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:55128bdeba99c44016902f6c01cde9386850a24903aa710a53c4a7edaea7700f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.4 MB (389382149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e95a2922360c266f1f8f42475157dc50dc9529e7386b24c767bf31f2b4563a7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 20 Jan 2024 03:41:37 GMT
COPY dir:8f7245a97c061726fd1f5e8ec557a254660d588f51008b0475bdcdcce3a48bba in / 
# Sat, 20 Jan 2024 03:41:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 03:43:14 GMT
ARG version=1.8.0_402.b08-1
# Sat, 20 Jan 2024 03:43:47 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 03:43:50 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 03:43:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cd4602cb0e84e00e8b7d38510ab92c4d091288133108bb74e581c22d31377e8b`  
		Last Modified: Fri, 19 Jan 2024 19:08:42 GMT  
		Size: 52.2 MB (52244936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11dcea0a6dc30e2b1814a3024b434d2b97a837e6ec398fa829eb8575287942ed`  
		Last Modified: Sat, 20 Jan 2024 03:52:44 GMT  
		Size: 278.5 MB (278458795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d75f438ec18e90e99ac91381a35133f34da467ea3d1256498dba3744ec3e9a84`  
		Last Modified: Sat, 20 Jan 2024 04:52:28 GMT  
		Size: 49.2 MB (49197132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14ce6bf03dad8d36be2c6abd6eaaefb16d9512faef5fb3acbbb340550267047c`  
		Last Modified: Sat, 20 Jan 2024 04:52:26 GMT  
		Size: 9.5 MB (9479909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f356fa01ff0ac0662c7c4c8e7bca403f710c009d213d7861cd59330bad19a7`  
		Last Modified: Sat, 20 Jan 2024 04:52:25 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dac0970e58847764e8d23c8b607fbf3c9684a17fc5c9396221abad1d9b912dfd`  
		Last Modified: Sat, 20 Jan 2024 04:52:25 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c340e70d51ed4adaed5e7399266263ea600588773202ee61dc1434613c3adc5f`  
		Last Modified: Sat, 20 Jan 2024 04:52:25 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:70400ac906e7923c22658d6c126f36cd4840eb8e7ee3a7d043dcb02270d8cc9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.5 MB (227489887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1ed195693b857f7dcbf2aee27f44094a1706de7a697d6b59ad37ee18aa7072`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:30 GMT
COPY dir:da17a174bd602e575391d08ca94d5595606a8d6d7b3b957cdec78f5fad499e19 in / 
# Thu, 01 Feb 2024 23:30:31 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:47:49 GMT
ARG version=1.8.0_402.b08-1
# Thu, 01 Feb 2024 23:48:04 GMT
# ARGS: version=1.8.0_402.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 01 Feb 2024 23:48:05 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:48:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 11 Dec 2023 11:12:11 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 11 Dec 2023 11:12:11 GMT
ARG MAVEN_VERSION=3.9.6
# Mon, 11 Dec 2023 11:12:11 GMT
ARG USER_HOME_DIR=/root
# Mon, 11 Dec 2023 11:12:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 11 Dec 2023 11:12:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 11 Dec 2023 11:12:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:d111cbc02b249a552b77e87298e3df2ce29173bc39b7d82aecba5ca8a2ab06d2`  
		Last Modified: Thu, 01 Feb 2024 00:30:08 GMT  
		Size: 51.3 MB (51322438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fa9f28c33d908cd2030f4eeb49e20eaa242931de8560e09cde54deebeab2f2`  
		Last Modified: Thu, 01 Feb 2024 23:58:19 GMT  
		Size: 118.6 MB (118555080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bd24ba7f10edad3dd995d63ad57a5b999aa7a14674892b8a7f34f13d6da6683`  
		Last Modified: Fri, 02 Feb 2024 03:46:30 GMT  
		Size: 48.1 MB (48131043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bc7b86923b76a38782ecfcdc8bddf10cc26a4566a5ccc72bd2babef7c138b7d`  
		Last Modified: Fri, 02 Feb 2024 03:46:28 GMT  
		Size: 9.5 MB (9479948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c626bd4248f7342c360a23275cdd99a105ec3011d53416a61f66201b6e8e1216`  
		Last Modified: Fri, 02 Feb 2024 03:46:27 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180ea7f845d3485390e8c1b9ed298fcfd16578b5c19d1545d7e99192a4108193`  
		Last Modified: Fri, 02 Feb 2024 03:46:27 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01f6e013d4c244127c63d6117580fd7d4d3246af93df4f37c3edf7c67684b024`  
		Last Modified: Fri, 02 Feb 2024 03:46:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
