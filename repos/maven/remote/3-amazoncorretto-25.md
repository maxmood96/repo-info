## `maven:3-amazoncorretto-25`

```console
$ docker pull maven@sha256:77edda77beb2eb546dbc0862a39026b745fdb94cb09a7eafd3fc4efd9ce84b89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25` - linux; amd64

```console
$ docker pull maven@sha256:cce9c1905570529f728380adca581e84bc0f5bb84fd3117b423200f4fa69c6e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384460643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:178cb3743321a816d481b542572adc5dda13149b06b279a828fc08b1023ffc90`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:09:15 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:09:15 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:16:15 GMT
ARG version=25.0.3.9-1
# Tue, 16 Jun 2026 01:16:15 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:16:15 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:16:15 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:16:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 16 Jun 2026 02:23:11 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 16 Jun 2026 02:23:11 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 02:23:11 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:23:11 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:23:11 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 02:23:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 02:23:11 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 02:23:11 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 02:23:12 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 02:23:12 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 02:23:12 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 02:23:12 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 02:23:12 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd44d40bd5b8f538bd043478c7f8bfcafc04f3a3a27b15f9231ff3acd91c7a8`  
		Last Modified: Tue, 16 Jun 2026 01:16:40 GMT  
		Size: 189.4 MB (189412755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:818565cfb01f3afcf85348c770dc6986e93386a2fa34888c89667a88c264ce4b`  
		Last Modified: Tue, 16 Jun 2026 02:23:30 GMT  
		Size: 131.1 MB (131115746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcf86021de3039deba261aaf222f959df22dd79ba6f7916b8b189c6e5294cde6`  
		Last Modified: Tue, 16 Jun 2026 02:23:27 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffa5c320b790636b128ed9da3834d76ff159a5c9444beea7c6c08be807eb6534`  
		Last Modified: Tue, 16 Jun 2026 02:23:27 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2499d8956001262fc2a0ffdce7c61fecc42741c79298e8daa3ffafd890eadeb`  
		Last Modified: Tue, 16 Jun 2026 02:23:27 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:fa7cf118d1ba03735812d07deeb143068b6c46eb45b01644b182de1c5a5486fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f00ad77afe78c63fd54ae2277624e957699acdbfc65ff0493ff86285ef014f65`

```dockerfile
```

-	Layers:
	-	`sha256:c1c11589a36233cfa20073c75f37a4ed757c9e4e5178d8371b69ca6a53e1d553`  
		Last Modified: Tue, 16 Jun 2026 02:23:27 GMT  
		Size: 6.2 MB (6216271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f506e3e71600d41d870ded79810bec175077fcd9b8bb3260969fa38418017402`  
		Last Modified: Tue, 16 Jun 2026 02:23:26 GMT  
		Size: 15.7 KB (15709 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:07b2b0b74682375af08f33b69acf1b9a0c102d63a7ad66b50afa1867a02f1054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 MB (380179445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87a57fb0ffe95130b2388150a9895db8736b8960b4dea66d4f71e81ae5b70bc9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jun 2026 00:10:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jun 2026 00:10:26 GMT
CMD ["/bin/bash"]
# Tue, 16 Jun 2026 01:17:31 GMT
ARG version=25.0.3.9-1
# Tue, 16 Jun 2026 01:17:31 GMT
ARG package_version=1
# Tue, 16 Jun 2026 01:17:31 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jun 2026 01:17:31 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 01:17:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 16 Jun 2026 02:24:04 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 16 Jun 2026 02:24:04 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 16 Jun 2026 02:24:04 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:24:04 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 16 Jun 2026 02:24:04 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 16 Jun 2026 02:24:04 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 16 Jun 2026 02:24:04 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 16 Jun 2026 02:24:04 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 16 Jun 2026 02:24:04 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 16 Jun 2026 02:24:04 GMT
ARG USER_HOME_DIR=/root
# Tue, 16 Jun 2026 02:24:04 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 16 Jun 2026 02:24:04 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 16 Jun 2026 02:24:04 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9225181157827e8afe6b6e29e476737d88a7af31a53eb9317eb2c87ab556b1a3`  
		Last Modified: Tue, 16 Jun 2026 01:17:56 GMT  
		Size: 187.3 MB (187327596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97af6336eddf983664a050a91685b7efefac7d97cc93faa4619c03c3ea1afcfd`  
		Last Modified: Tue, 16 Jun 2026 02:24:24 GMT  
		Size: 130.0 MB (130033038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4eb431bbfbd80470bff70cf59182a5210374292b1e94bf543b741ac5dfd48a9`  
		Last Modified: Tue, 16 Jun 2026 02:24:21 GMT  
		Size: 9.4 MB (9359972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afc9e88274692ea74dcedfdfa30ec924784b7472574c2b7e319fb8163431663`  
		Last Modified: Tue, 16 Jun 2026 02:24:21 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa4f308363164898adf1cade833d2039ec53418fa3cac3c144457af8c1d7f9f2`  
		Last Modified: Tue, 16 Jun 2026 02:24:21 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25` - unknown; unknown

```console
$ docker pull maven@sha256:fe3da1e61bc4b73f0571008933427ed4e3f91d1513877e92106c9c39b41a2783
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d637369a9df230388c7f396605166cf1727dda8ac39ddb72faa528ed6395518`

```dockerfile
```

-	Layers:
	-	`sha256:0e0cb7dea37951e0f322d58aa783ed8bde744088c4a8051d8ae807599694dd56`  
		Last Modified: Tue, 16 Jun 2026 02:24:21 GMT  
		Size: 6.2 MB (6215264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbf3c468c0d5ddc9b3a78d008f92b8dff49038e04054be94b0a8a247db11f01a`  
		Last Modified: Tue, 16 Jun 2026 02:24:20 GMT  
		Size: 15.9 KB (15891 bytes)  
		MIME: application/vnd.in-toto+json
