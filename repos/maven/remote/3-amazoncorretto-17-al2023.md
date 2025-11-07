## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:9aae99327d976474ea7ada380cc4735446cecabd398a70fdf3ead03268ab7e70
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:fe0e6efa38d285c6a3a4842ee78a5d684b270e4a4881f4b878c330e4c7b1bd43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.3 MB (325274121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62be5434685c5b9f6a421150d9b1baf98c4a65040e2e4e6b0a959d8d73e8049c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:05 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:05 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:05 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:05 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 31 Oct 2025 01:14:50 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:14:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:14:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:14:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:14:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:14:52 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:14:52 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:14:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:14:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:14:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc93996f720aafe561378567487aad4cac58bd5c93215d7c30b4dc3cb269fe7d`  
		Last Modified: Fri, 31 Oct 2025 01:11:05 GMT  
		Size: 156.9 MB (156930995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7f1f568e5e548bac7f3fb0a9098f908f3d48c5ac1c6690cc0ccfc22d85d3f84`  
		Last Modified: Fri, 31 Oct 2025 01:15:36 GMT  
		Size: 92.6 MB (92577985 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44496049a0981323b75aad987a3905cefdf6916dff0a5d50a97bcc01ab74f7d5`  
		Last Modified: Fri, 31 Oct 2025 01:15:21 GMT  
		Size: 12.5 MB (12520272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee6a5932334ca9c62ff6198915efa020dd003c76a231d66b143d9e9f670fe7bc`  
		Last Modified: Fri, 31 Oct 2025 01:15:21 GMT  
		Size: 9.2 MB (9242591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2e11c65a705f8d9deacf2ae5d556d06d9714eef61deba99933dcd3c552f3c7`  
		Last Modified: Fri, 31 Oct 2025 01:15:20 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1392124a4ef65514a25a79fe4fe4c378d350d4a43035a16b5cf8b00866d6f696`  
		Last Modified: Fri, 31 Oct 2025 01:15:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:7ebca544f52668742fb3378534187be82edae3eaf8fa6480d16a8234483a7969
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405dbdf5dc7b990cbad6cf34985de7ef5430036a55f618fa79e9c8e4eb6925b3`

```dockerfile
```

-	Layers:
	-	`sha256:cab2d5e0abc6943d04803c17649988ec68bf4c8e5a90049a1f3e47456c83f0e3`  
		Last Modified: Fri, 31 Oct 2025 02:27:59 GMT  
		Size: 6.2 MB (6232024 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aaee8344e3e8561f3a22a8a81ebce94b2d1a611eb8ef2f6c2712223bae5c4431`  
		Last Modified: Fri, 31 Oct 2025 02:28:00 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:3af8f3b8ecaf8e28b3f6f49770f678c7a5f42776cfa5c90502bed4b3420e1979
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **322.4 MB (322384121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a8c2769b0e5cb97866d2b93e9a6874cffe94c372d1ff46c39bda166749c147e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:13:29 GMT
ARG version=17.0.17.10-1
# Thu, 06 Nov 2025 22:13:29 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:13:29 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:13:29 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:13:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 06 Nov 2025 23:15:01 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 06 Nov 2025 23:15:05 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 06 Nov 2025 23:15:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 06 Nov 2025 23:15:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 06 Nov 2025 23:15:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 06 Nov 2025 23:15:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 06 Nov 2025 23:15:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 06 Nov 2025 23:15:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 06 Nov 2025 23:15:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 06 Nov 2025 23:15:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 06 Nov 2025 23:15:05 GMT
ARG MAVEN_VERSION=3.9.11
# Thu, 06 Nov 2025 23:15:05 GMT
ARG USER_HOME_DIR=/root
# Thu, 06 Nov 2025 23:15:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 06 Nov 2025 23:15:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 06 Nov 2025 23:15:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42206444f43ddda96491ceb64db5c92fe941fa16f8ddf5f9800eaf678742c975`  
		Last Modified: Thu, 06 Nov 2025 23:11:31 GMT  
		Size: 155.7 MB (155740957 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fdb1129511d521a6a2e1c7765af663de4865aeeed802bfaee79fd4dbf924b38`  
		Last Modified: Thu, 06 Nov 2025 23:15:38 GMT  
		Size: 91.7 MB (91720042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b5aff1146d3fdb914dea89297334bb3c2e69012eb14b47533863b12fa650aa`  
		Last Modified: Thu, 06 Nov 2025 23:15:29 GMT  
		Size: 12.8 MB (12777799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e281b9fd79f9182fcff64a2472a18edd47c75df0f555a6c7be500b721376930`  
		Last Modified: Thu, 06 Nov 2025 23:15:28 GMT  
		Size: 9.2 MB (9242595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff36e480cf24537838d63adebd10c32c8e64994e0b26887b3162088fe4854fec`  
		Last Modified: Thu, 06 Nov 2025 23:15:28 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4194e00e33c5b2027c60f0c5db27935a852972feeafa7cb3b268963866f7c9f`  
		Last Modified: Thu, 06 Nov 2025 23:15:29 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:a162ec22feede2b54335f9f026ab9a5f067374d12596c9e9a13a03aca9fbce47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad99037a6215a054b26dc08e21855c1639320eb066e06ed04a689dbfd81139c`

```dockerfile
```

-	Layers:
	-	`sha256:fa3e6a1fa4be8aeda242d7fc000860067398cd886ca09d1859962ab0ff5c3dbe`  
		Last Modified: Fri, 07 Nov 2025 00:27:57 GMT  
		Size: 6.2 MB (6230954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84ebbb6c407ccb30c078fb9f2e85d4fecb791240872c7466b3f979edf3e88890`  
		Last Modified: Fri, 07 Nov 2025 00:27:58 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
