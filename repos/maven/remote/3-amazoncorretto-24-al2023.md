## `maven:3-amazoncorretto-24-al2023`

```console
$ docker pull maven@sha256:ff1d09a2868098ce5a94c4535a1c1e46d6b3aa25f499e88f36fb8de180bf1fc7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c0b534e0c4a9ab86390b64ddd74b035fc8d2eb486bb1555b20409222881e52c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **346.6 MB (346624506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0633be631aedd6b6f0f626f9beafa2d51933560c04e929ca00305413de45ddb5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 29 Jul 2025 19:33:31 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 29 Jul 2025 19:33:31 GMT
ARG USER_HOME_DIR=/root
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 29 Jul 2025 19:33:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 29 Jul 2025 19:33:31 GMT
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
	-	`sha256:53b5c8da72d4b8a6e061bde6874a4aa1db4950be515570304cfc5c1b41b83224`  
		Last Modified: Fri, 12 Sep 2025 02:11:45 GMT  
		Size: 96.1 MB (96112864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9132dc4e5298a6080af5d9c5a312983afcd8ac210c37c72e116545a8261b6298`  
		Last Modified: Fri, 12 Sep 2025 02:11:26 GMT  
		Size: 9.2 MB (9242569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a41fa8a27015052cb8ee7f4ee4d8852118050b5e9de7975beb12062829ccc2b`  
		Last Modified: Fri, 12 Sep 2025 02:11:23 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbcd708aa49aa4be13bcba00c66b4dc1f484948fb08a5aa4a8686649826a0c3`  
		Last Modified: Fri, 12 Sep 2025 02:11:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:2ee3aa2195de5a0b1d9a69d8f64d86b0bc05e9d054b88b2c4a3ef24f098eec4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eedcd304f1d2b5d61f83c795d171b2478aa5eef17bbdae31f143cc23d951cfc7`

```dockerfile
```

-	Layers:
	-	`sha256:e1603dc63f532393e4eaa37f33a7fabd34521ba681daeaff76b02711e322e192`  
		Last Modified: Fri, 12 Sep 2025 05:28:35 GMT  
		Size: 6.2 MB (6207698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8993aabd413c299d06fd822dcd1c5dc208a58f079e86a08a8baa30c2ce08f075`  
		Last Modified: Fri, 12 Sep 2025 05:28:35 GMT  
		Size: 16.4 KB (16388 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6ea1012e53be4467e5815b0b17ada49346e1e4c769d5533561fad326e35bf2f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.9 MB (342918446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0db042cf9b503dcb6fbbcbbad14d8cb6dd9dc53c90457d7df77a670bac5adf45`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Tue, 29 Jul 2025 19:33:31 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 29 Jul 2025 19:33:31 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 29 Jul 2025 19:33:31 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 29 Jul 2025 19:33:31 GMT
ARG USER_HOME_DIR=/root
# Tue, 29 Jul 2025 19:33:31 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 29 Jul 2025 19:33:31 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 29 Jul 2025 19:33:31 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2133584a03a0323a461f4ba1900a168268d3305d6206a4e0a210c92b146e94a`  
		Last Modified: Wed, 10 Sep 2025 02:34:05 GMT  
		Size: 52.8 MB (52775111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2cbebd879707334eb7f2f9a2a52fcbb43995964915e992b4dc087015d3dc3c`  
		Last Modified: Fri, 12 Sep 2025 02:11:14 GMT  
		Size: 185.4 MB (185434865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d07ae3110178d6c4755a9ff161bb8b095a9c3be3efed2c0d0241989be2a70cbd`  
		Last Modified: Fri, 12 Sep 2025 02:16:06 GMT  
		Size: 95.5 MB (95464842 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c181608e8ce8d29f5934358255e2856882929e2c71cf6c57589feadc2189b7`  
		Last Modified: Fri, 12 Sep 2025 02:15:54 GMT  
		Size: 9.2 MB (9242586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3aa65df0f5ea560de987f419c0da91ccb52d2d8312f52b5c72d0ffcb610d99`  
		Last Modified: Fri, 12 Sep 2025 02:15:52 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603a33800378eec4fd97398f9cc5acf5ca48d590bcbd931a5d7cbda0cb445f90`  
		Last Modified: Fri, 12 Sep 2025 02:15:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:f579a447172a6426239666685dc85597872e086bf0466e43f2b1c8b091a54fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93128c2030d82f17fbfd695699af350dab45bc6574adefc64525383f3868d479`

```dockerfile
```

-	Layers:
	-	`sha256:d6ce1c818b42dd1528149a894b331092f67200e17e5dde73fd9201c8f91fbf62`  
		Last Modified: Fri, 12 Sep 2025 05:28:41 GMT  
		Size: 6.2 MB (6206642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c13e6f4217ca36d83d63171363245646b19f1d9dba344f937aa3cff640eb572`  
		Last Modified: Fri, 12 Sep 2025 05:28:41 GMT  
		Size: 16.5 KB (16520 bytes)  
		MIME: application/vnd.in-toto+json
