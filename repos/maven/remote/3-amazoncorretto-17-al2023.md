## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:27739dd1d529ba74e6623a5229d4ad859d099f33259ddb4c8c64f0d31f834f42
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7af9a52870d95abe4a88f7ed1b5f33506383f3d129d5c00b938810208f2aaa71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.8 MB (290798635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f836f84eefc40e13112bf02586cd4e85fd5db56ff34f621ad8e764baf8e12df4`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:351cdd1ae1934b18a2b9071735ba92b02b0a1b8775e2a03f31fdaf06f2fba243`  
		Last Modified: Mon, 16 Dec 2024 23:59:50 GMT  
		Size: 53.2 MB (53156313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5859f9641afaa836ca11cc6020a849fe64059acf5f0a845ca5418373b68473f3`  
		Size: 156.5 MB (156499341 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:392b755424dc8b05a4ffa5dfb41e0bce256bc8e5ab16d6e604fcb2c08c03a862`  
		Last Modified: Fri, 20 Dec 2024 23:16:25 GMT  
		Size: 59.4 MB (59427748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0084dcc83a7e7dd53c8b1ed59a7989c32ea2d15a8773be1d665fe3f6f9615373`  
		Last Modified: Fri, 20 Dec 2024 23:16:25 GMT  
		Size: 12.5 MB (12543748 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b717bc563b7e58eb92885a4e3502deeea6c651bd78a1e5f50ca0902479534309`  
		Last Modified: Fri, 20 Dec 2024 23:16:25 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0ae25befdb6b51371181256877c86ca8ac90ca47b3a3b54cd32a5203b02c50`  
		Last Modified: Fri, 20 Dec 2024 23:16:25 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e7dc9e793b3eacc1e139bff1f5200a1d4e71ff6af789aa170f47b3d3a6aa54`  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:00504fd4a2777d49faea7ec71655695cbe0673e4c0f4444eea69b10433bab20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6241790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:315509afb6c14033300a81fe150af74567a133d0152d6ccd08dc29bf46e65cf7`

```dockerfile
```

-	Layers:
	-	`sha256:9ff458283d242a8c5f00e5806a839ec1d3a9c2f3fb1950fd425fed478d8a391e`  
		Last Modified: Fri, 20 Dec 2024 23:16:25 GMT  
		Size: 6.2 MB (6223475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7e9a3c01361e8924039bbed5009d77c0eae22b56cccb37e3aa2c2ca57a2cd897`  
		Size: 18.3 KB (18315 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ca680a62b2e53cfa840d1f7ccc20239daa1b2ef9b46266758246503d19daeb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **288.4 MB (288367680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:511ccc66932f7dfb0e41e1c30e79cfcb8f6646c1950c888d73836a48b6999e0e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=17.0.13.11-1
# Tue, 20 Aug 2024 18:12:59 GMT
ARG package_version=1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:98ab3ce9b55607064b358289eeb810db43f69e016067c07e7136a807475f6f27`  
		Last Modified: Tue, 17 Dec 2024 02:01:08 GMT  
		Size: 52.3 MB (52276382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e1981df7f486f8d183ce6429bf697ef30b63336d1daeb7a0c2f57abaeb4008f`  
		Size: 155.3 MB (155309017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7035af8503f4e8385a42ef747728a4e0f64a47178837c545eea6af5c529bc33c`  
		Last Modified: Sat, 21 Dec 2024 04:56:38 GMT  
		Size: 58.8 MB (58799682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15061ad6409758d7baa4838b49ed11fc94526d0d8657def1531d8cf4f6ca3e29`  
		Last Modified: Sat, 21 Dec 2024 04:56:36 GMT  
		Size: 12.8 MB (12811130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df395f499ab3431a29edff2d4855bad991efeece920c18e9809499fbb9c7245c`  
		Last Modified: Sat, 21 Dec 2024 04:56:37 GMT  
		Size: 9.2 MB (9170424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:207a850e3baf16af9fbb015ff807faad6cab1f9c67eceb7569456ee1d9be37ae`  
		Last Modified: Sat, 21 Dec 2024 04:56:36 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a12df8a379ca17e3beddab50b000a266c4c5dfa296b53d4ac2de9de6dfe250a3`  
		Last Modified: Sat, 21 Dec 2024 04:56:37 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1576bba3e080a171eb65197b3260740f36608b9616377c1e8a8668c4c745ae86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6240869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22a701cb14e96723203cf46cad59433f66e60736680b609d5a27daf26745da50`

```dockerfile
```

-	Layers:
	-	`sha256:ebf2ffa68b43f8b8dfafdb2911baece5ce5d1be4b3655fc8347ae7729683e721`  
		Last Modified: Sat, 21 Dec 2024 04:56:36 GMT  
		Size: 6.2 MB (6222405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:68d4db9b19be9971fbee01ecafcccc7fa22b9994f8a1c59ccde65d548b06e61f`  
		Last Modified: Sat, 21 Dec 2024 04:56:35 GMT  
		Size: 18.5 KB (18464 bytes)  
		MIME: application/vnd.in-toto+json
