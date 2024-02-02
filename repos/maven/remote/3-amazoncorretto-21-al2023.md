## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:f0888834be2809a7198cf069bfeb578fdce92a54f9050370f12d5aac950c93ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:8267c8ef641ff5567648ad0250019de23c66498329b3667e9e46e4b405469c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.0 MB (280007610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac1397ce77c12fd41f0c6bc36401c1330a22d1e973a6328bfa44cdb0a14dc56`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 20 Jan 2024 03:41:37 GMT
COPY dir:8f7245a97c061726fd1f5e8ec557a254660d588f51008b0475bdcdcce3a48bba in / 
# Sat, 20 Jan 2024 03:41:38 GMT
CMD ["/bin/bash"]
# Sat, 20 Jan 2024 03:49:17 GMT
ARG version=21.0.2.13-1
# Sat, 20 Jan 2024 03:49:17 GMT
ARG package_version=1
# Sat, 20 Jan 2024 03:49:39 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 20 Jan 2024 03:49:39 GMT
ENV LANG=C.UTF-8
# Sat, 20 Jan 2024 03:49:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:b86c5beb98e15b711ec9631e022897faa8f8a99e2ab6b47b02981a333bf49600`  
		Last Modified: Sat, 20 Jan 2024 03:59:20 GMT  
		Size: 170.6 MB (170581099 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f4b314cfac263aac23b900cb45d521f58e9d13e6efabaf9eada0a61b9056422`  
		Last Modified: Sat, 20 Jan 2024 04:51:47 GMT  
		Size: 47.7 MB (47700290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a69388c7860cebaf1f9da8151976bb8393705b148c1968f6b1024e92e4993fa`  
		Last Modified: Sat, 20 Jan 2024 04:51:45 GMT  
		Size: 9.5 MB (9479908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3382dca2ac3e451a97ac093bce7afd2072ec931cb377450e5ebda5b02eaee4b`  
		Last Modified: Sat, 20 Jan 2024 04:51:44 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79bd5848edf94ca935d41e9ce01b41bd0ba161ebaab4514a1006de15365fdd8`  
		Last Modified: Sat, 20 Jan 2024 04:51:44 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4faf5f13131fdfab719e700a4e9e5b9fa5661fc349eef984362e1745e6ece340`  
		Last Modified: Sat, 20 Jan 2024 04:51:44 GMT  
		Size: 165.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:21529a5539e084e21510d3566887cb1dc91f5982328710a1b8a4cc8c25943cbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.7 MB (277714823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9863f5a5cc0ce861ba71f8f08eac7dd64a53745620f9c09774bf1f0b197eabea`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:30 GMT
COPY dir:da17a174bd602e575391d08ca94d5595606a8d6d7b3b957cdec78f5fad499e19 in / 
# Thu, 01 Feb 2024 23:30:31 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:26 GMT
ARG version=21.0.2.13-1
# Thu, 01 Feb 2024 23:55:26 GMT
ARG package_version=1
# Thu, 01 Feb 2024 23:55:46 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 01 Feb 2024 23:55:48 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:55:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:88e1eb677f88689798344a21fa0c6bb876a608edf9ae1f8dcf544e13da7afc82`  
		Last Modified: Fri, 02 Feb 2024 00:04:45 GMT  
		Size: 168.8 MB (168769897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0167e381bbd638c06efc564ba4695c93432e43b36dec052c780a9ec763ecad7c`  
		Last Modified: Fri, 02 Feb 2024 03:45:55 GMT  
		Size: 48.1 MB (48141165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c22762b6cfda02d568f4c2a86ec8d11a3bf5d4759b6e8aea39145e417d218459`  
		Last Modified: Fri, 02 Feb 2024 03:45:53 GMT  
		Size: 9.5 MB (9479948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d26f7e2f28ec30ff82f87a49454cfd502d90d33da3b528b4edeacdbc6e2e3e6a`  
		Last Modified: Fri, 02 Feb 2024 03:45:52 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0911c10552a773445d555910cc5c5950b7755a47fcd252a07f0a29b680d4d1d`  
		Last Modified: Fri, 02 Feb 2024 03:45:52 GMT  
		Size: 355.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdf33558dfaa06cd217c93d8c12a9f75a17d36bfd9a02d4d896a418e5c8aa9cb`  
		Last Modified: Fri, 02 Feb 2024 03:45:53 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
