## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:908b1b7e1d2ba88806807b5b573db3b3dd69447127826333f7a444b45a3302c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:6bbd640a27f8a781a86fe9c3146e4466d5893a2ee26f3928ef35a6c5b71552b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354748068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99f782cd3234f0d10428619e5b4f2f0ae22862f50c83237071e580cee70d7980`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:07:15 GMT
ARG version=25.0.1.9-1
# Wed, 05 Nov 2025 01:07:15 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:07:15 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:07:15 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 05 Nov 2025 05:03:14 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 05 Nov 2025 05:03:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 05 Nov 2025 05:03:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 05 Nov 2025 05:03:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 05 Nov 2025 05:03:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 05 Nov 2025 05:03:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 05 Nov 2025 05:03:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 05 Nov 2025 05:03:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 05 Nov 2025 05:03:14 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 05 Nov 2025 05:03:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 05 Nov 2025 05:03:14 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 05 Nov 2025 05:03:14 GMT
ARG USER_HOME_DIR=/root
# Wed, 05 Nov 2025 05:03:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 05 Nov 2025 05:03:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 05 Nov 2025 05:03:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68c1f44d1f333eca771d4302a52c66b724492a443b32096a502dd680573ad6f9`  
		Last Modified: Wed, 05 Nov 2025 04:48:51 GMT  
		Size: 189.2 MB (189168084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58d3eebd0eb99c40526050d17a026de3690500a01bb9965ce744ad9c92c39bbe`  
		Last Modified: Wed, 05 Nov 2025 05:03:59 GMT  
		Size: 102.3 MB (102335114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25d71d536c4e430183dfe544eea17f9944097168b7cf52a940a5457805ecc80`  
		Last Modified: Wed, 05 Nov 2025 05:03:45 GMT  
		Size: 9.2 MB (9242594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fc5fe69ec9e31c83a5ca64c79294ed791fc66f7f59c7c9cfaf568e5ea8be673`  
		Last Modified: Wed, 05 Nov 2025 05:03:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f61f098e9f4203f800649325a825fa44a99e470b487f223bf628bc0d332297a5`  
		Last Modified: Wed, 05 Nov 2025 05:03:44 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:9d36f3d648917465573a4814836b6583040c85d3e49f415ccee1a1666f98952f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7122e91a657c70cd33f1660edfa10d79b0eaf700e9869023a5854fa1f758a39c`

```dockerfile
```

-	Layers:
	-	`sha256:b994ffa586199b128602c3e25c8629dd7680bfc2b82a0f116f6171e7c3a760ca`  
		Last Modified: Wed, 05 Nov 2025 06:27:46 GMT  
		Size: 6.2 MB (6207774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7d42028450625f80c0283642c0c8ed70321c76a2680af3581c8fca8b55939e4b`  
		Last Modified: Wed, 05 Nov 2025 06:27:47 GMT  
		Size: 16.3 KB (16349 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ee03b78cc794d2a38aec4491d3b9e719ae2b51759dafa46bd1d7cb02c71e66eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350989383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:767cf729cde9d9a4d488996b8c4d2336aee68a3b36857b9b30c34bdd3813244b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:39 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 22:14:39 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:39 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:39 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 06 Nov 2025 23:15:41 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 06 Nov 2025 23:15:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 06 Nov 2025 23:15:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 06 Nov 2025 23:15:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 06 Nov 2025 23:15:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 06 Nov 2025 23:15:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 06 Nov 2025 23:15:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 06 Nov 2025 23:15:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 06 Nov 2025 23:15:41 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 06 Nov 2025 23:15:41 GMT
ARG USER_HOME_DIR=/root
# Thu, 06 Nov 2025 23:15:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 06 Nov 2025 23:15:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 06 Nov 2025 23:15:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123460810639ecd99796c2d04c9c602287fe1bbb2613c2622aabd5176f1a2c40`  
		Last Modified: Thu, 06 Nov 2025 23:10:36 GMT  
		Size: 187.1 MB (187092407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a1c180f353c6e19d11f825714a9eb2bf2444a3ec61f1c01fb97ba30f7e7cb4`  
		Last Modified: Thu, 06 Nov 2025 23:16:23 GMT  
		Size: 101.8 MB (101751661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e5a87150d2a4aad22493ddb6f2064f08aea6c60654f5a934cdd4c0ba499137`  
		Last Modified: Thu, 06 Nov 2025 23:16:08 GMT  
		Size: 9.2 MB (9242585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1afaa63b9a6f1a32e5cb1ef3beb5ab4fb618269b26c2129509aef8c898b1778`  
		Last Modified: Thu, 06 Nov 2025 23:16:07 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c9f273690f86fec20b7c87fd98ad2a702d6a3d6d42a3a98145e2cfcc95e7f60`  
		Last Modified: Thu, 06 Nov 2025 23:16:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:f33747032acce73ae6726711cbd4428b357a549cae46bb2897e4261b387fda3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e894905ee3ea75cfa502e121eef4ddf5141a068235849ae347635bb8287499a`

```dockerfile
```

-	Layers:
	-	`sha256:d1fc4ae8f47d2d67ad26dff0e5bb787caeb2ea211ba9b63eb310ddc422e95e26`  
		Last Modified: Fri, 07 Nov 2025 00:28:21 GMT  
		Size: 6.2 MB (6206718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15bef949c0f73ccfec31b977eeb3a867586fb1a9390b2075a098822c8d975a8`  
		Last Modified: Fri, 07 Nov 2025 00:28:22 GMT  
		Size: 16.5 KB (16481 bytes)  
		MIME: application/vnd.in-toto+json
