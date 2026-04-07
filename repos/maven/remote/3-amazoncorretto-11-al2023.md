## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:90f1f279b35c83177bab1ec70a11bc858cfd0d586f74ea0877381a3017731ed0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5b9a15d551691a7ee7af7027a4a04917ac8e144e7af6ce9b29ed416e92ae86e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.9 MB (338879399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719998c77df1ec0fa9a213948e6290fc218a209aafdea9904780f17a7b8f1273`
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
# Tue, 07 Apr 2026 05:07:25 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 07 Apr 2026 05:07:28 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 07 Apr 2026 05:07:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:07:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:07:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:07:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:07:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:07:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:07:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:07:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:07:28 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:07:28 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:07:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:07:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:07:28 GMT
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
	-	`sha256:6577158275a9eaff36d59c835cb02287bb5315b01e586c25713c719b460f4e78`  
		Last Modified: Tue, 07 Apr 2026 05:07:48 GMT  
		Size: 109.1 MB (109098099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b034d5a99c6d48ec065367874025a8f6ee78d845caa22af3f930f6de292428c7`  
		Last Modified: Tue, 07 Apr 2026 05:07:45 GMT  
		Size: 12.5 MB (12533160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95a3fc8ee8d201001b5a04d812dada1e77fac23f73b2c158c660c96958e2e1d9`  
		Last Modified: Tue, 07 Apr 2026 05:07:45 GMT  
		Size: 9.3 MB (9311189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b66a7de162e195a8a97dfdd0ce6bb4d3923d81203fd559d1bb0a6bdae560b9`  
		Last Modified: Tue, 07 Apr 2026 05:07:44 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a891a24af80fe978ec4ce6fb34caa4536bf317d5b1f6abcb5f6e45b9d56fd1e`  
		Last Modified: Tue, 07 Apr 2026 05:07:46 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:4e3c1a53204139ad2d06a1193d9e0c8d7a25080ba8c4d823b031bebf6121d371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4128d2177bb13f1b5db263cf5339aa55676b29d02e86c0ccd695fc8a6cd881`

```dockerfile
```

-	Layers:
	-	`sha256:07482d7eb27c4c32578afbc4972b2f6bbd2b4d008937ee9593feca527ea8ac34`  
		Last Modified: Tue, 07 Apr 2026 05:07:45 GMT  
		Size: 6.3 MB (6263967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3744e3c76e3e0b2ea6c6348471ccfd2c4a3854d70360c13c8367fd661b1318d7`  
		Last Modified: Tue, 07 Apr 2026 05:07:45 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:907d94ec809e730581642d4798f6f5c13fb2da1999ad995da34e64061984b704
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.4 MB (335361261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4fdf6bc227df84fd13e26c7904f98003392b8ea6dfbe8dbda6a22d2b6799b20`
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
# Tue, 07 Apr 2026 05:13:45 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 07 Apr 2026 05:13:47 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 07 Apr 2026 05:13:47 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 07 Apr 2026 05:13:47 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:47 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 07 Apr 2026 05:13:47 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 07 Apr 2026 05:13:47 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 07 Apr 2026 05:13:47 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 07 Apr 2026 05:13:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 07 Apr 2026 05:13:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 07 Apr 2026 05:13:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 07 Apr 2026 05:13:48 GMT
ARG MAVEN_VERSION=3.9.14
# Tue, 07 Apr 2026 05:13:48 GMT
ARG USER_HOME_DIR=/root
# Tue, 07 Apr 2026 05:13:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 07 Apr 2026 05:13:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 07 Apr 2026 05:13:48 GMT
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
	-	`sha256:8e716bde9ffd5694637cdcfb947bf88dc9d09327b30bbc8dcd01c4105242b79c`  
		Last Modified: Tue, 07 Apr 2026 05:14:08 GMT  
		Size: 107.9 MB (107888415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8617c7044d290ac47f44c58dca5b081e1d0d821e993bc50da6290b240b1e34a7`  
		Last Modified: Tue, 07 Apr 2026 05:14:05 GMT  
		Size: 12.8 MB (12794281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b773fa35ad956063689590c5f4aa40ef8ebce929c116efe4ec62f975dbff6142`  
		Last Modified: Tue, 07 Apr 2026 05:14:05 GMT  
		Size: 9.3 MB (9311173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e05bfaf76b5967bf4671c99d8d9d50aeef14c05ddd126241465c40381f5b08c`  
		Last Modified: Tue, 07 Apr 2026 05:14:05 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188d7bb339187407e3083f5b1c8003dcbb59f1e6ff573dd492ed2ab62b1f69bc`  
		Last Modified: Tue, 07 Apr 2026 05:14:06 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:179c38c7a241eb37a85c637a2890322765a51008cc0e67863aa8a29ccbc200ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6282180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ce2d04377778ec8c32850fb7bd18ffc7273ac99e68219debdf26e67339f7040`

```dockerfile
```

-	Layers:
	-	`sha256:c00524851f1a9924687e01ece56ea35d3ba54f5322e9004670b6c5ad64c9882a`  
		Last Modified: Tue, 07 Apr 2026 05:14:05 GMT  
		Size: 6.3 MB (6263741 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23a2243df741681fca24ff8d8e2928f495abc5d934a26cbac7a9f07eaa01fc63`  
		Last Modified: Tue, 07 Apr 2026 05:14:04 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
