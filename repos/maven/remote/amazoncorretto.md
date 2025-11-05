## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:8da9f1d92ddf819a3c70adbc816ddd5bc4ad27dc846972458e800ab43f7764e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:3def2cba46d5067d6173b7358b44283cf64128f4af2924c4c70df321e7b70e55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.7 MB (354745729 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3760bb1dc017fb36e3b2b1f7804961999482bdd29a57132dce06de6555192c71`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:49 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:12:49 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:49 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:49 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 31 Oct 2025 01:15:39 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:15:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:15:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:15:39 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:15:39 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:15:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:15:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:15:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cad330e08d585bcff7ce7b398a5a2dbb684e338ae4fe298f9dca43f057f4b8c`  
		Last Modified: Fri, 31 Oct 2025 01:10:53 GMT  
		Size: 189.2 MB (189165602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d72c56bb0ac84bf845bc967e83b73f0e85b102264a8d9ddcf72db95839a623a`  
		Last Modified: Fri, 31 Oct 2025 01:16:15 GMT  
		Size: 102.3 MB (102335259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5adae163f3920c60b30fc9fe88530471b259a69ca8bd27e767a8c3f8c11d6ddc`  
		Last Modified: Fri, 31 Oct 2025 01:16:03 GMT  
		Size: 9.2 MB (9242592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:206917bc618f02e534706d307d4426a3eb4dd15f7b4a32f216aa803ac5cfb5f3`  
		Last Modified: Fri, 31 Oct 2025 01:16:02 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dc38e3dcdcc88c730b6c022c80c7534721f97a4a9952d3437bb6ea2de122f3f`  
		Last Modified: Fri, 31 Oct 2025 01:16:02 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:fa3bf40060009715dbd6e06c8ee0bfd8ef0be2c86424b3b61144a8d30cdb9204
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff665c534ae69fc481583c9d4f039bba99632e9fe4245697225e26c0b34f1925`

```dockerfile
```

-	Layers:
	-	`sha256:6eb587c8d88ab8bc9e94ce9e0d59c50a09fbc5bf666bb4a48960fc93b39a3471`  
		Last Modified: Fri, 31 Oct 2025 02:27:23 GMT  
		Size: 6.2 MB (6209006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8300d29b77bf7dd441d4079104feb96a4eba84be519bc4416cb7f32e7368a6a1`  
		Last Modified: Fri, 31 Oct 2025 02:27:24 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:949f128b6acc15cfa04b6a9e32dad37601741cb463c8f096c2fbfa5a1d5b3b50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.9 MB (350894135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e81d736af915970ad3b98e8eee0a1ad1bdb61fe7af94bf279aa7a5c80ebdf3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:16:48 GMT
ARG version=25.0.1.9-1
# Tue, 04 Nov 2025 23:16:48 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:16:48 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:16:48 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 04 Nov 2025 23:27:19 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 04 Nov 2025 23:27:19 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 04 Nov 2025 23:27:19 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 04 Nov 2025 23:27:19 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 04 Nov 2025 23:27:19 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 04 Nov 2025 23:27:19 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 04 Nov 2025 23:27:20 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 04 Nov 2025 23:27:20 GMT
ARG MAVEN_VERSION=3.9.11
# Tue, 04 Nov 2025 23:27:20 GMT
ARG USER_HOME_DIR=/root
# Tue, 04 Nov 2025 23:27:20 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 04 Nov 2025 23:27:20 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 04 Nov 2025 23:27:20 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9365c25afe64e4be1bd920de12cba12a4866ebadce41ee02775bebe9869913ec`  
		Last Modified: Tue, 04 Nov 2025 23:25:30 GMT  
		Size: 187.1 MB (187092250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7577b72361f1a7be63cb2cda982b4927a7fe191baea718271a0661de58ed706`  
		Last Modified: Tue, 04 Nov 2025 23:27:57 GMT  
		Size: 101.7 MB (101656406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02497aa030ede5e70b901554496af2bbad6739c447c95ce19bc0403715d06265`  
		Last Modified: Tue, 04 Nov 2025 23:27:46 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ab922cb52bb0c9103a479d8d50e591738b1f7557e7f4c3e8dfb331d71d4138b`  
		Last Modified: Tue, 04 Nov 2025 23:27:45 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a5c84d4f138ff44da479ba1f0280ead4cb8b3ecd499665483ffcf285b65084e`  
		Last Modified: Tue, 04 Nov 2025 23:27:45 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:13817ed40b6082ee35c5af2cd79cd87a6edc5f1bd4e11023ce8de14d85866e75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3621af07641924d4835d24e3f3d43756d6ade91b83317b8fed8acd20aa5a01b`

```dockerfile
```

-	Layers:
	-	`sha256:0a92d22bc234bd753b8791de75ddaed76d69eee43cdd3fecfc44c947a75b668b`  
		Last Modified: Wed, 05 Nov 2025 00:27:41 GMT  
		Size: 6.2 MB (6207998 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9caecad075a2744d6cabed6606c85cccedc7bc5d466608155697c6dfceab9763`  
		Last Modified: Wed, 05 Nov 2025 00:27:42 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
