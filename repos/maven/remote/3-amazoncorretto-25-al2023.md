## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:a2ccfa4c42893caafe116e6bfb02fdc21af9652a5f513752014bf1bd4d1c7c27
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2de080faf53a01b5d7ed718d6316c98accdc9f794c8c06217a77dd0c539ebc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **378.4 MB (378407523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b5cfecbefcf6bcdd0e6282640842fe54eb71d2e2b37ad58903482a6bd73b9b8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:55:56 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:55:56 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:19:00 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:19:00 GMT
ARG package_version=1
# Sat, 09 May 2026 00:19:00 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:19:00 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:19:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 09 May 2026 01:25:45 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 09 May 2026 01:25:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:25:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:25:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:25:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:25:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:25:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:25:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:25:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:25:45 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:25:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:25:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:25:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c6daf6f5f632799e37bfaf0ead2057112cc6402948c88e815dfb2bb78f8f7aa1`  
		Last Modified: Tue, 05 May 2026 12:54:11 GMT  
		Size: 54.6 MB (54576804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0250ec3d728132a010a8ee425e754a8d5a13a96838c49f810421351398ab603e`  
		Last Modified: Sat, 09 May 2026 00:19:24 GMT  
		Size: 189.4 MB (189411044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00ec8e792579caefd43ecff807fdfa83c53c573e72978cab7b4a166c1b52adc`  
		Last Modified: Sat, 09 May 2026 01:26:02 GMT  
		Size: 125.1 MB (125106414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e392c3a83705dfd7d68010c0cb2eb946a41b60bf78bf93b4c29bb84427648c9a`  
		Last Modified: Sat, 09 May 2026 01:26:00 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7c51fd25caf472b1d154d54a80b1121290af304d9129fb364714236aaba7a6`  
		Last Modified: Sat, 09 May 2026 01:25:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32b1e5260183836a6ad523e6b5c424a02763505de6298371e2239729b63470f2`  
		Last Modified: Sat, 09 May 2026 01:26:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e0a3dbd1625d4ec9a3301b2e6ec1791fd97827ee07573a47928515105cf1547e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba478219bd8a1116a00eea69cbcc1a096595cd8761019d4acab0f9938ba812b1`

```dockerfile
```

-	Layers:
	-	`sha256:fc9ad93c9af336fe39b79e4ed4195f8f3d0d74db27628d61554b84086fa02e76`  
		Last Modified: Sat, 09 May 2026 01:26:00 GMT  
		Size: 6.2 MB (6215036 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30951639ce3f190b53a46bca8a12cb6ca314e19116f1bdbb409e33b237280552`  
		Last Modified: Sat, 09 May 2026 01:25:59 GMT  
		Size: 14.7 KB (14661 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f1a03e297860a86796b0382e37efa65639b39db8c3502ab62c88fae348c4ef7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374232175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1055d9e0bdf2224e114418b1964e56b4eda72338e721418a7c67488e609fc665`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 08 May 2026 22:48:12 GMT
COPY /rootfs/ / # buildkit
# Fri, 08 May 2026 22:48:12 GMT
CMD ["/bin/bash"]
# Sat, 09 May 2026 00:16:48 GMT
ARG version=25.0.3.9-1
# Sat, 09 May 2026 00:16:48 GMT
ARG package_version=1
# Sat, 09 May 2026 00:16:48 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Sat, 09 May 2026 00:16:48 GMT
ENV LANG=C.UTF-8
# Sat, 09 May 2026 00:16:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 09 May 2026 01:49:44 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 09 May 2026 01:49:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 09 May 2026 01:49:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:49:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 09 May 2026 01:49:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 09 May 2026 01:49:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 09 May 2026 01:49:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 09 May 2026 01:49:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 09 May 2026 01:49:45 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 09 May 2026 01:49:45 GMT
ARG USER_HOME_DIR=/root
# Sat, 09 May 2026 01:49:45 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 09 May 2026 01:49:45 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 09 May 2026 01:49:45 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8ce1f9c92d5e473d6cc57893a4bae88accbdce44b631fbe2bb3a1d2975254fab`  
		Last Modified: Tue, 05 May 2026 12:54:04 GMT  
		Size: 53.5 MB (53456975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:650af40d683d967f6be2238c5da49e6232e999e2dbcf6f6803931dde1fea81a8`  
		Last Modified: Sat, 09 May 2026 00:17:16 GMT  
		Size: 187.3 MB (187330634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b317e0476a5e5af9df8594831d0ac6d5676118c7de23da51ef005ac2b493fcd`  
		Last Modified: Sat, 09 May 2026 01:50:05 GMT  
		Size: 124.1 MB (124131305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f59bc597321890fae4dc0de346985e406cb47f78f1cb93cb984d341d093513`  
		Last Modified: Sat, 09 May 2026 01:50:02 GMT  
		Size: 9.3 MB (9312253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6369d786702021b121d5af44e618086d14c64e49d2d162f1faa7c9c53e46f15f`  
		Last Modified: Sat, 09 May 2026 01:50:02 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:094a4f91107f32967812c100d570065a3360945669fb7d0ef1bbf94e42b14fe7`  
		Last Modified: Sat, 09 May 2026 01:50:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:96807223004af85b62351ffbcb4a65bf262372b6907cc7192fa2bbabcdd91ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6228775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440b329e18f70c17ff91cc0ddd5e0e4c764d8fd31cf92b438dc14d29f749f97d`

```dockerfile
```

-	Layers:
	-	`sha256:5aff878f5eba597bd8e0fa88f2bada27dad43e986c59c938764594d48579cedd`  
		Last Modified: Sat, 09 May 2026 01:50:02 GMT  
		Size: 6.2 MB (6213981 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcb311a42fe79fb0157fa371464df683f517cb45da4ccf79adbd1f14fd105ffc`  
		Last Modified: Sat, 09 May 2026 01:50:02 GMT  
		Size: 14.8 KB (14794 bytes)  
		MIME: application/vnd.in-toto+json
