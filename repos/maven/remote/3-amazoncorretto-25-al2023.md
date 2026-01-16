## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:220ad2f33d3caaecadec211ef1b8c9ca3e01034ce9a37977d885313d32ca57d9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:aef30f09b1044a8e2916d62d337e1219231b6acefb241dcd4be815500deaa34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.4 MB (361372319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4ed72f1f7d75d7d8161e064c4981f8a1358fbf54e6466e822167588b0d1cce`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:10:13 GMT
ARG version=25.0.1.9-1
# Thu, 15 Jan 2026 22:10:13 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:10:13 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:10:13 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:10:13 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 16 Jan 2026 02:46:17 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:46:17 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:46:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:46:17 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:46:18 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:46:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:46:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:46:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:46:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d88fe3c4b256f3e9e43b9cb5ec26a56a3f9a83b14d7daf8a3ab39250d61c86`  
		Last Modified: Thu, 15 Jan 2026 22:52:23 GMT  
		Size: 189.1 MB (189137832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76433b2ed5646a0ec3700a629a89b609030af35c87aff44a98de4983b18ec5aa`  
		Last Modified: Fri, 16 Jan 2026 02:47:11 GMT  
		Size: 108.9 MB (108900000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ebb78d5b633280803eb6233298f7d53eef3b264de5b3d0e1a4a4d44f977a97`  
		Last Modified: Fri, 16 Jan 2026 02:46:56 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:102837aaa2cef13acb28abd6225bc0ae07b262cde0aef736cda8d56913efe47a`  
		Last Modified: Fri, 16 Jan 2026 02:46:55 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e5afddb26672c42763a41c386372d64cf9a760b9a418aa4fe4e1cbc6fa7cc06`  
		Last Modified: Fri, 16 Jan 2026 02:46:42 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:0eb462a82acef21fa2721b5a3fbb093b7ff90752ffb32b27c7d47e2e75619346
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:719e040493e11e036d5d55252e6171660f99f67b599bae2b253fe5c9d1b40628`

```dockerfile
```

-	Layers:
	-	`sha256:ea873ab6e3b4c405038f287cc24bfa662a7c195e0192176fbdcddc4a34e9e636`  
		Last Modified: Fri, 16 Jan 2026 03:29:37 GMT  
		Size: 6.2 MB (6207785 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77f6780aa8ab4c1e6f3a615296095dcc4ad087993d2b8e87d45b5ed5415a159f`  
		Last Modified: Fri, 16 Jan 2026 03:29:38 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4e0fc144aebc2172760b4df71e3d611b532a9a7f7fdccd95618052b270c0d5a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.3 MB (354271001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd7803366a14b80bf9a214f3c0fb54eb7ba6461abc702d5ad36b5073ead51b16`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:27:35 GMT
ARG version=25.0.1.9-1
# Thu, 18 Dec 2025 01:27:35 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:27:35 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:27:35 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:27:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 18 Dec 2025 02:23:41 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 18 Dec 2025 02:23:41 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:23:41 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:41 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:23:41 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:23:41 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:23:41 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:23:41 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:23:41 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:23:41 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:23:41 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:23:41 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:23:41 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:23:41 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:23:41 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:612c39deef61a58a025e6feada7d5e61866b65d460e5d2e64f4d258c21076418`  
		Last Modified: Thu, 18 Dec 2025 02:18:45 GMT  
		Size: 187.1 MB (187059395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1269313a092fca1f556f080eefcac642e56602f40a6889f8789c1edf74c6e341`  
		Last Modified: Thu, 18 Dec 2025 02:24:28 GMT  
		Size: 105.0 MB (105024873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5ef6cfab80ca0d0e620839b046be5c1952f3b3f588e92eb6206bc32a56640eb`  
		Last Modified: Thu, 18 Dec 2025 02:24:10 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22890c5e3019b121fe17250d0089fddbb4ac382f848e6dc376963df198b80fa4`  
		Last Modified: Thu, 18 Dec 2025 02:24:07 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b1de17103def036e4010a9be46a27010c6ac4db93e56e3ff97672c8fad49799`  
		Last Modified: Thu, 18 Dec 2025 02:24:07 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e535dd364afbfda4ade22e8a47ec83e0c71ee0ff6c3e42072bf622e230ad10e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f067a722ba9c61e1e43534a2cd6ce35700de99931cc8ba17788a70acf9a29a22`

```dockerfile
```

-	Layers:
	-	`sha256:46b90072baa9817ae7252809a0dd454e90207a41123d2a6168f8d05f337ca662`  
		Last Modified: Thu, 18 Dec 2025 03:28:39 GMT  
		Size: 6.2 MB (6206725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3267cddc9c0463955619e1c59e97a1a6d63883344dc6b70ca7896451af67cc9c`  
		Last Modified: Thu, 18 Dec 2025 03:28:40 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
