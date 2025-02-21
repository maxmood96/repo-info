## `maven:3-amazoncorretto-23-al2023`

```console
$ docker pull maven@sha256:83874598db82558194d77f9d617134527a997e64a674e50a89453145ea5d6663
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-al2023` - linux; amd64

```console
$ docker pull maven@sha256:9f1847b3d9912c37861a1a300ade5c7a0c375b88964d45c81fff0e66a1dc585b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **311.4 MB (311365465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ee53650643b5e6aa746ecf48e5a7f655a778aa9ebb950d97afa7b3f1f178edb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.2.7-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:878bc77d48b9be49ba0c1a9449cd773b9ec0a7bf22d5286569e4011e441370c3`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 53.2 MB (53150583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8073932606b83d7e36d356d36cf30841afac184f1873b5cf0eb2460f423146c8`  
		Last Modified: Mon, 10 Feb 2025 20:08:51 GMT  
		Size: 177.6 MB (177576982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677e1d2e4e85c508bf43d628bdf921ce7ea8a07534b5da1c68962f83c6308994`  
		Last Modified: Mon, 10 Feb 2025 21:08:27 GMT  
		Size: 71.5 MB (71466428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b6f92bc1a7c11173f1abb561ff22b590ccb61a2f4b618898bc0fa20888a625`  
		Last Modified: Mon, 10 Feb 2025 21:08:25 GMT  
		Size: 9.2 MB (9170431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:233e5de87055ecd8810bd3d5924149e90d1e2b184d738c97caef22342b61e650`  
		Last Modified: Mon, 10 Feb 2025 21:08:25 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42d1945369d72dff9f90865968d8bee465f42f77941e4591f4798f6f2122cc24`  
		Last Modified: Mon, 10 Feb 2025 21:08:26 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:28977f0e1300b13509b7db7a8d6ff162f8f78707980a33a3cce9cb614e06ba6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6186816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5459b477355e03c59e3a34c40f4909438558cf220ae880f3fab30d61b0cc3d`

```dockerfile
```

-	Layers:
	-	`sha256:d77378e232cb47041310fbd8669870ab60b8cfd3429c82aa01ae19fcaf7b237c`  
		Last Modified: Mon, 10 Feb 2025 21:08:26 GMT  
		Size: 6.2 MB (6170439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b218db10c4f1fe028652ab98899d41af49283d9da54687ad4ab9f517b27aaf80`  
		Last Modified: Mon, 10 Feb 2025 21:08:26 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:5d74e21ea621902fa7f22065fd706359d23d20c5e54886b55c17500d37ee8e1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308373586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe06783d76ed4a7a7f0dfca37618eac67717a85a3ffd4f49a00559e5de65d713`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.2.7-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc3f95e28e80d0726f0a42fc5782fe710190034937206e3e830873d8e426ba4`  
		Last Modified: Mon, 10 Feb 2025 20:29:43 GMT  
		Size: 175.6 MB (175608456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d980973aa551ed70b1a977d128d4d3d8406905cea803704eab2f1e1db7688ed`  
		Last Modified: Mon, 10 Feb 2025 21:33:56 GMT  
		Size: 71.3 MB (71322705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4ce1af86b1b668ec029779df442027846da463ff4bf1b63317a090a90284a0`  
		Last Modified: Mon, 10 Feb 2025 21:33:54 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffd7ec5753b5ce28763d9368cbd16e094f3316a39fd9b99fbdfa8a14b64a59a5`  
		Last Modified: Mon, 10 Feb 2025 21:33:53 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebb088a60dd673422b7a611031c163f610dfdde258f509dbe807568585ae55c`  
		Last Modified: Mon, 10 Feb 2025 21:33:53 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:28464378497208459ed30baf5b360cb53510feb8f65dda56e23ff578fdb0b957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6185069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ffb05bed0beb8b5fecde79c0dcbb4934e3388834d08901fca617b953b1af5f`

```dockerfile
```

-	Layers:
	-	`sha256:ec45133e0c568323aa3efa6cd13518f15e9a0ea668bbb60d892ff6354f321425`  
		Last Modified: Mon, 10 Feb 2025 21:34:10 GMT  
		Size: 6.2 MB (6168559 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b540c30327efee2c3457a7035588af77c1c10d3d0a5c7d7695fd7d322d88c042`  
		Last Modified: Mon, 10 Feb 2025 21:34:09 GMT  
		Size: 16.5 KB (16510 bytes)  
		MIME: application/vnd.in-toto+json
