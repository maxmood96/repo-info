## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:0afccde9692ef2f5f89cf4d0cfacdf550e70a76a6e815a8064d0a7530e07e7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:6caf28cae12b66060fbb6080f135c0ca483dbcf47ad9740bf9f3db1b5376fdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.4 MB (388380128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64eca86ac2acde5c3dac0d34c0aec8fcf5c5b25643a5013b45e9347de2774ac`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:25:10 GMT
COPY dir:c7d5463abe17dfd3879bd12c94f31ebdaedb939167b5199c40650e35e379f334 in / 
# Fri, 19 Apr 2024 22:25:10 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:49:51 GMT
ARG version=1.8.0_412.b08-1
# Fri, 19 Apr 2024 22:50:25 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:50:27 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:50:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:6f59c9417334b7a9eb6449cc09a14d6738ae8afbfb25d681f2c27740e7d4856c`  
		Last Modified: Fri, 19 Apr 2024 22:25:53 GMT  
		Size: 52.3 MB (52323609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91ab07dd353945d07adcee3e5f73d96c66c34ecc9197df9c4b3c10c8c03f4233`  
		Last Modified: Fri, 19 Apr 2024 23:05:32 GMT  
		Size: 278.3 MB (278316802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88192725d61004d1e490f2f2be4c7239e5399e61e6992dc22cfc311855cd38c4`  
		Last Modified: Tue, 28 May 2024 19:58:31 GMT  
		Size: 48.1 MB (48090771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:410805149d1d67674688255a2bbd85988a7045cf52f30b90416f3e8987d60823`  
		Last Modified: Tue, 28 May 2024 19:58:29 GMT  
		Size: 9.6 MB (9647569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099215b85970ab64539e1c07cec268af49e8c818ccca8a76b61c54d53aeac6b3`  
		Last Modified: Tue, 28 May 2024 19:58:28 GMT  
		Size: 852.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c2eb3f4a64cf2110a603f94fb6ef4f410963e9ddc7d1f51f4dc9561ee73893`  
		Last Modified: Tue, 28 May 2024 19:58:28 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b767e22a38b041b7ee1916a24bd561d0bf05fc4cf7f0ba0ae9f2d0a2661d51af`  
		Last Modified: Tue, 28 May 2024 19:58:28 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:cdd6ef0d752ada28f7bee79eb1f323d5889eb9ae54085215a833411cf5f68fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.8 MB (225840246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9af4d56c365054d2a5d60798aeb343badc41328f3c21f0a0b86d8f51e1fba2a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 19 Apr 2024 22:10:28 GMT
COPY dir:e8d306065b89c24e8d7ed76b1f4a499224cd18e3ec44dc6823b5d039220ebc19 in / 
# Fri, 19 Apr 2024 22:10:29 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:28:39 GMT
ARG version=1.8.0_412.b08-1
# Fri, 19 Apr 2024 22:28:58 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:28:59 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:28:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:0fff0db406e493d5737bccd8db4b9460e6d6c5e6d45f62e14ae7cb208fcc984a`  
		Last Modified: Fri, 19 Apr 2024 22:11:04 GMT  
		Size: 51.4 MB (51413307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9ec501b96453b06d8f52928ac3bb69771da4a563f6ce33401912dfb3beb6421`  
		Last Modified: Fri, 19 Apr 2024 22:41:00 GMT  
		Size: 118.6 MB (118556021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3333e158f2b4c7cb6c125e96ab8644cd1a8eb4996de2a7a3b432aad1143c8beb`  
		Last Modified: Tue, 28 May 2024 20:38:38 GMT  
		Size: 46.2 MB (46221980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70354d54ba018540017e02f165563be62068f67650bd1de38754828565b5723b`  
		Last Modified: Tue, 28 May 2024 20:38:37 GMT  
		Size: 9.6 MB (9647556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e99bf25dc84c2dc82ae11fdf82f8f6472a4a5d6f3d52fba8abd01c62e073b50b`  
		Last Modified: Tue, 28 May 2024 20:38:36 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adfdd9cf61febdf1414714026cba691cbffa5304af31556112af630ec716dbaf`  
		Last Modified: Tue, 28 May 2024 20:38:36 GMT  
		Size: 360.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3a24b4b090f8d541f2f9e8da76406a030875e9fb21f24ccb2953aec6583aad`  
		Last Modified: Tue, 28 May 2024 20:38:36 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
