## `maven:3-amazoncorretto-24`

```console
$ docker pull maven@sha256:8f35c3f4e0dcfd73f9ee5c3dd40363a42ec2035604907334b9a5785d910a39de
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24` - linux; amd64

```console
$ docker pull maven@sha256:42036b4e682536f97a624b1c8901c806a0971397d46457748c259c6c2d0f5a50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.6 MB (346624560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62faea4da08e92345db23c2a152304fea4e2fef4aa07cc97883cc8dc30ea4da6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0727f841555e830a24054117b5d53ecc18438e2e82fc78dd3cc766ca6bb76cab`  
		Last Modified: Wed, 10 Sep 2025 02:33:49 GMT  
		Size: 53.9 MB (53875706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04f5546491ed02b9f45eaa39cfd205fc6ab018e0405337dce3b527b11e3bca6d`  
		Last Modified: Fri, 12 Sep 2025 02:10:15 GMT  
		Size: 187.4 MB (187392324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0430064bdc846ab6f695bf7cdabe93f418c808c95923978b1671ed6683e25659`  
		Last Modified: Tue, 16 Sep 2025 00:17:58 GMT  
		Size: 96.1 MB (96112924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6af53234572ffb2fce09d6ca75976372c0b8fa6b7474fa3c57553d05c6ee668`  
		Last Modified: Tue, 16 Sep 2025 00:17:36 GMT  
		Size: 9.2 MB (9242565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b967c9feedbfbc2aad46d29bb4585f8caaa243ac6027322f188f5b80e545a345`  
		Last Modified: Tue, 16 Sep 2025 00:17:35 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94fcfdfa52db0a1f74b3e1c4ff52be922158253177f5968b8351bab4dfa29f8c`  
		Last Modified: Tue, 16 Sep 2025 00:17:35 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:ed2534b167bc1e7a02699e28ab7a34f1c9d84b5c8c13693fcff0f3f330c413df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53b049cf3a5c29e3dbd2350fa72872a67de60c07483fdb824b565f7b8a96cdb2`

```dockerfile
```

-	Layers:
	-	`sha256:e83f39bb76d2fcddc27597534fdf39bea258a4aeb59f40ec5f75994c12e91ef4`  
		Last Modified: Tue, 16 Sep 2025 02:29:00 GMT  
		Size: 6.2 MB (6207656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4342783f489d3e5c1a2b08f28f93ae5e269acd70ac28c093d68dd071e3c9abe`  
		Last Modified: Tue, 16 Sep 2025 02:29:01 GMT  
		Size: 16.3 KB (16312 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:fd798557b0d1fd77c510ebfd7114a2b30291bef8ac0ee3b56be7df6f11e4d72c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **344.4 MB (344417361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28d218c18e46bf6c22034a4993961f818ad8fea1c4cbf34727962d64a89aad76`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=24.0.2.12-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946b11b9ef98756026bddbaf5330fbbdae8f538a9cdd2415bc38f8ddcd65509e`  
		Last Modified: Wed, 24 Sep 2025 22:11:11 GMT  
		Size: 185.4 MB (185436531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7017e20597ee3ad07e89c715e7c4e190f2aec7fcb5e37cc011120a3b2b870649`  
		Last Modified: Wed, 24 Sep 2025 22:16:09 GMT  
		Size: 96.8 MB (96837771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f4bbd48a7a8e85c2b01de328c07d9f259e255717351d7ae8f7a4b511dc4bb4`  
		Last Modified: Wed, 24 Sep 2025 22:16:01 GMT  
		Size: 9.2 MB (9242580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223fa737624e4e39fdbce7011565cb8d6429fd1b83044026390bff01f96d3182`  
		Last Modified: Wed, 24 Sep 2025 22:15:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6dd3bce645ce709ae6b63b65b3818fe665e7eaf6207b03be7c5962d00a188ef`  
		Last Modified: Wed, 24 Sep 2025 22:15:58 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:fac88a974a8c50f882b531cc97a709bfecd62072150d74b7751720eb02a790c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e63afea8b3be6e18ad56e098fd22027e11b136b4852d0f1eaafba6ce6ae8af9`

```dockerfile
```

-	Layers:
	-	`sha256:dd7256ac8f377de0db67886068e4f8b3918889c5928a0e606d427efa0a2e507e`  
		Last Modified: Thu, 25 Sep 2025 02:28:07 GMT  
		Size: 6.2 MB (6206600 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb9e447c8573be84b13f230c7c718e61eeb2c39f3ceb6e12170a3e227c92436a`  
		Last Modified: Thu, 25 Sep 2025 02:28:08 GMT  
		Size: 16.4 KB (16446 bytes)  
		MIME: application/vnd.in-toto+json
