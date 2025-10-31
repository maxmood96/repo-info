## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:7710bb5f5bed9df6c2b1947156536400d8d393e2d77e88d5994d34d21f5a83ac
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:da9ab4477422bded90d49f78a49f96c795b31d99de45204287812154e19b875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.7 MB (321696401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b67b23c216ec8c3ee3192db7e7c975e791365b0322113071dd6905c2256c000`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:25 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:25 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:25 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 31 Oct 2025 01:14:32 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 31 Oct 2025 01:14:35 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:14:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:35 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:36 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:36 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f643f97c106e8b010a5e3ab951bd53f9b0f08ee366ac0330e4641b14e18fa31`  
		Last Modified: Fri, 31 Oct 2025 01:11:37 GMT  
		Size: 153.3 MB (153345023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3611cb35fbf8979e15eaa842abfc9e71856f207a00a65c01a66207e402995ad`  
		Last Modified: Fri, 31 Oct 2025 01:15:16 GMT  
		Size: 92.6 MB (92580965 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3b490eab726d178c045171a6f5a6c7a636a4b4d8f2e1ea24b7b969b50687df8`  
		Last Modified: Fri, 31 Oct 2025 01:14:59 GMT  
		Size: 12.5 MB (12525542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cbe97a98b2821f0b448b6c9b83f20693ebe0a880a0f58276b3ab6962e671e7`  
		Last Modified: Fri, 31 Oct 2025 01:14:59 GMT  
		Size: 9.2 MB (9242594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d455247200b01a60df3db3090fef60e5516a35a1e399cae60aaea3b27622e7d6`  
		Last Modified: Fri, 31 Oct 2025 01:14:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078d7ce9586456c76ea399634584bfb47f8b9616c5382a8b40fe7b97db8dd12d`  
		Last Modified: Fri, 31 Oct 2025 01:14:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1f09ebe9f9e3a0de429a5037ad5034b32150a4db42d37d5d968f38aa741a6ba0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57c5f39461adbe9625a728e9aa7ca6f18526d6b05fba3ab0de0a91f917227f2c`

```dockerfile
```

-	Layers:
	-	`sha256:858bce0e04b60dd3b08b768ab47b663fc974276d34ca6e9b9255abafe94296fe`  
		Last Modified: Fri, 31 Oct 2025 02:27:41 GMT  
		Size: 6.3 MB (6257524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c66de8f5441f5222aa31e113c75ecda1b12edf90db33dbefc3ad05122290a83`  
		Last Modified: Fri, 31 Oct 2025 02:27:42 GMT  
		Size: 18.3 KB (18284 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:da20bcf5d1b80b874ecd5ba32f6bb26750c5d589cfd63cfa749194aec513cd55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **318.4 MB (318445109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a606cf018eb351cad73354d0ba22e10a320ab2e46929c0393ef5df062b05accf`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:04 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:12:04 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:04 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Fri, 31 Oct 2025 01:14:42 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 31 Oct 2025 01:14:44 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:14:44 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:44 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:44 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:44 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:44 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:44 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:44 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:44 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:44 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:44 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:44 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:44 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:44 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9da5c775d769db73a4fca8aa53fc2f2b6b1a89bd48619b51d0173aade89e5888`  
		Last Modified: Fri, 31 Oct 2025 01:12:11 GMT  
		Size: 151.9 MB (151892338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9a98f47a00faf52e50c08c81c57f560ca37c7c048facfee5d4b59650c64879`  
		Last Modified: Fri, 31 Oct 2025 01:15:21 GMT  
		Size: 91.6 MB (91627299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f064cd35e58436ecaa503b33e03c6043485dbbeba21353b94a23bfad11a83afe`  
		Last Modified: Fri, 31 Oct 2025 01:15:08 GMT  
		Size: 12.8 MB (12779990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3903677f2ba08c766a788633fbede4fc632809e31756592cf110438c896df0f2`  
		Last Modified: Fri, 31 Oct 2025 01:15:08 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3cac4fa9c9c2770e60c0fee4d777295208b8132391225fc781da0df213dcdcb`  
		Last Modified: Fri, 31 Oct 2025 01:15:07 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ac149296cf7f8b7806da30a3685641d22d8be271736d5979aaaab3c26c8e33`  
		Last Modified: Fri, 31 Oct 2025 01:15:07 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:b5eb4305c088b533eeccf6fbe5d773267c83d1465529ae9d0a91b323db38bb3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e529938a0d776b577e31cf8410b7e7ad4ecab6fd317fd320f0f96423943643bb`

```dockerfile
```

-	Layers:
	-	`sha256:0398537e0921d1ce33bd6926bed0e6116f7f1182810558efb36a9ffa962145a8`  
		Last Modified: Fri, 31 Oct 2025 02:27:49 GMT  
		Size: 6.3 MB (6257298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4bcc6e09e8e2a2f6f35fcb589917e718bc4901260ba95e40f8f55b47d47d0a50`  
		Last Modified: Fri, 31 Oct 2025 02:27:50 GMT  
		Size: 18.4 KB (18429 bytes)  
		MIME: application/vnd.in-toto+json
