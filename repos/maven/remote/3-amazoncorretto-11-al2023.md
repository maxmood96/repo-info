## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:bcd5fcb66aca2b417ac2487e940fce1d40c5cb052d59d58b6a8f0b53741205a8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:3657ee4cef8a3caf9a4a2db56f249649f1f65c9429b0f81f3d3696fede7a7805
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338879440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea96463d7dc24a74d8b813802d358220ff597df12a97fb3f6bf1454b8a51b1ea`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:50 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:50 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:50 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 03 Apr 2026 23:14:05 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 03 Apr 2026 23:14:08 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 03 Apr 2026 23:14:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 23:14:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:14:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:14:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 23:14:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 23:14:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 23:14:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 23:14:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 23:14:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 23:14:08 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 23:14:08 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 23:14:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 23:14:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 23:14:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14afc2702a7f10f51001c183da30616257459b7a21460ae343e010ff2341af55`  
		Last Modified: Fri, 03 Apr 2026 22:14:10 GMT  
		Size: 153.4 MB (153364606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7bd773680f9fcf0f3db0b67d2f6ef098a757b176c26debb3c6043977118a67`  
		Last Modified: Fri, 03 Apr 2026 23:14:26 GMT  
		Size: 109.1 MB (109097979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:017f082d18a4036cd15cd85806c6e3c863fd22c2d20214dee78f56969ae2212e`  
		Last Modified: Fri, 03 Apr 2026 23:14:23 GMT  
		Size: 12.5 MB (12533328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaaffba2eddd8c654b8a2bbaaac071e09dd4f810223df131a40121773b397487`  
		Last Modified: Fri, 03 Apr 2026 23:14:23 GMT  
		Size: 9.3 MB (9311180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c06a0884f352246e6469471c5ced263cf12fc4f779465f3216f36e9a50fdb2`  
		Last Modified: Fri, 03 Apr 2026 23:14:22 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a57cf2abddc170316c0266705feee0c8a2567f85093b6f317a6e7670fabfdc6f`  
		Last Modified: Fri, 03 Apr 2026 23:14:24 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:bafba97c9c770448fab7c4d6f16ca153aab782714a6e8ab434c2bb47db4c6b7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4654352d38f365777c2798cdb5c8fdd4a1da093433d8443a0e9d02cfc6fb7204`

```dockerfile
```

-	Layers:
	-	`sha256:00fb6e468c051c0a5b0b3da430d4998c9b12b5d5882b98e58800d643d9ed8d6a`  
		Last Modified: Fri, 03 Apr 2026 23:14:23 GMT  
		Size: 6.3 MB (6263967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2518815d49ab3141ae7bbd25895f81e190abd9179560e5afb22c818e985f9551`  
		Last Modified: Fri, 03 Apr 2026 23:14:22 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:20e39843b8871c34779edd4aa873da4db168f3eab81a8fa369a764f6728733d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335361088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7c89689f78ff14ed9003fc765c87496adc9efc08f96709820311efa2d727897`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:47 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 22:13:47 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:47 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 03 Apr 2026 23:14:41 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 03 Apr 2026 23:14:44 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 03 Apr 2026 23:14:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 23:14:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:14:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 23:14:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 23:14:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 23:14:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 23:14:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 23:14:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 23:14:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 23:14:44 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 23:14:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 23:14:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 23:14:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 23:14:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49a77dccec3e92a918f77b51b05b9a494897149cb94761faec731163d8c68bc2`  
		Last Modified: Fri, 03 Apr 2026 22:14:09 GMT  
		Size: 151.9 MB (151923526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16596dc8f927a628d191f9ce0e560174231d342c0b3ab064abd1db7674e9c2e2`  
		Last Modified: Fri, 03 Apr 2026 23:15:03 GMT  
		Size: 107.9 MB (107888195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e38971816f3fe819bff75ac9211dcf42b63ab0d414b75bb4f8ae2e418cd1822`  
		Last Modified: Fri, 03 Apr 2026 23:15:00 GMT  
		Size: 12.8 MB (12794318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1d6cdbe4dae8438c39ea38036dbd09904682a1b4cac41c0c1e72fe3bb750e7b`  
		Last Modified: Fri, 03 Apr 2026 23:15:00 GMT  
		Size: 9.3 MB (9311181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10414437f16a91e661e531f3ae01416dc9434c6d205b3f7eba0453a92543656e`  
		Last Modified: Fri, 03 Apr 2026 23:15:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ee1924247f90faa8a538cf6faed95142a3032e1492f0a65d30458d57872c5`  
		Last Modified: Fri, 03 Apr 2026 23:15:01 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:3c7cab2b81c9cc691ae8b06308f747704baf7e30e9418d0503d8bf49230650f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:568f09e9e1b8b8c01448a54923e3f4f76637339b889715905471c8cd8a5683be`

```dockerfile
```

-	Layers:
	-	`sha256:f59eb38b59de59777ed2bfb38d79a58271919f1732e9dd9a3df1700c003f93a0`  
		Last Modified: Fri, 03 Apr 2026 23:15:00 GMT  
		Size: 6.3 MB (6263741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d72750b1c56958254aedd833a0a88dc3ba1dba17014210500124d1f239609025`  
		Last Modified: Fri, 03 Apr 2026 23:14:59 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
