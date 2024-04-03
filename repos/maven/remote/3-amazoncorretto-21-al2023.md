## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:15586cbfb959c7fac119a2dc80ee415e34873405420e7c90dcfafa34279f7728
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:ec62fb202ec55734f4b32e73ea8243694ac024b3a5d23f31ea0fe3958c3b711f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.6 MB (283564596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e71dee92065b3944246ad0d2f6c55fee46cc165803428671abd7a41b162446`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 07:58:56 GMT
COPY dir:a3b34d0fa41c44f27db0e1cc5fb85c42e2d376f97e37c993883bc79b0ac16bdc in / 
# Sat, 16 Mar 2024 07:58:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:41:53 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 13:41:53 GMT
ARG package_version=1
# Sat, 16 Mar 2024 13:42:17 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 13:42:18 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:42:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:47a7782bf36730e29aeeeb2bd36b1fc2a9d8b97f2ee4990a6ad2300602de69b0`  
		Last Modified: Wed, 13 Mar 2024 20:11:15 GMT  
		Size: 52.3 MB (52334338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6010f22f453f67f107ab74e240e085abbf52353a911819283c17feb3642cbdc1`  
		Last Modified: Sat, 16 Mar 2024 13:51:35 GMT  
		Size: 170.6 MB (170571284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeea02cebf8360da1390ed6ba7583621b232a7e0a8c35f34441101ed91576db3`  
		Last Modified: Sat, 16 Mar 2024 15:05:12 GMT  
		Size: 51.2 MB (51177648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f3d948edd0999055bd0f27fec8ae0a9e10ccd25c622510f92cad264ec8a5c59`  
		Last Modified: Sat, 16 Mar 2024 15:05:09 GMT  
		Size: 9.5 MB (9479945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed04af150ad1be3918d1b15582520377f166243aeb7fdc61b42c1346dd135471`  
		Last Modified: Sat, 16 Mar 2024 15:05:09 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3793c9f30a29421b9dbf18f289b614002a06841ee38f7b269dc4a7be4c5c4397`  
		Last Modified: Sat, 16 Mar 2024 15:05:09 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7958680bce0decde50b1dccda6b9c02f33a643dae68ef1cf9239d16e1906026`  
		Last Modified: Sat, 16 Mar 2024 15:05:09 GMT  
		Size: 167.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:0aa0f5cd153545d4001a6ee13dd9d6b33f1961d84762c505f9055b2380785412
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **280.4 MB (280424164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e177b1cbff05c94039322e4abb29c52d9f0972fc87ac4024f4163c18c133b83`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 16 Mar 2024 00:05:49 GMT
COPY dir:df28b18edcce192f5e6601a1f5352535de64369eb71fe3f006ea8b6aa29b9c84 in / 
# Sat, 16 Mar 2024 00:05:50 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:46:56 GMT
ARG version=21.0.2.14-1
# Sat, 16 Mar 2024 03:46:56 GMT
ARG package_version=1
# Sat, 16 Mar 2024 03:47:17 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 03:47:19 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:47:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:dd798988746a347b32a9e843088ef9c56978b6beca831a29a02bcd2ca002cea1`  
		Last Modified: Wed, 13 Mar 2024 20:11:17 GMT  
		Size: 51.4 MB (51414586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994930751f3db3ec6c7821403863fe9df3a5e1d2d5597f7496f8593e86bff166`  
		Last Modified: Sat, 16 Mar 2024 04:01:20 GMT  
		Size: 168.8 MB (168775634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195a61f88e4b97bf06af71eb88da13ae4feaf08487256cb3ed40411cb7e3efe4`  
		Last Modified: Sat, 16 Mar 2024 13:04:53 GMT  
		Size: 50.8 MB (50752632 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1ca7fcb7db1ca7bfbfd311a3136238a59756121788b93ec0915df4c1a3d26ef`  
		Last Modified: Sat, 16 Mar 2024 13:04:51 GMT  
		Size: 9.5 MB (9479932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9313283d6fc2cd24b52aaefe06feceb5e399e9309e46f7c946a414eac607e062`  
		Last Modified: Sat, 16 Mar 2024 13:04:50 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceebca62ea4a3456b99de16f29fb5a6e117890b79dfbb693531cb08f7bdfaab1`  
		Last Modified: Sat, 16 Mar 2024 13:04:50 GMT  
		Size: 361.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eebd4a85cc02f13e0b65473ae3d29702ee151f92b48bfed495c117b4561d1e9`  
		Last Modified: Sat, 16 Mar 2024 13:04:50 GMT  
		Size: 166.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
