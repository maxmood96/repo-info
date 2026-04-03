## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:75b896d11d2dbaa30a0a37a7e9e689581644587f3ba88958ece553acc94f970b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:bc8a636b935127841ddbcc3e4543f47d7325dc1b18413810591ec9fe1bb6fefb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.6 MB (351583631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d5e85b314dc8419b8882cbc97c1ab19fbc2cd8be6c3da51b92f27b25bf597`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:09:28 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:09:28 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:09:28 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:09:28 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:09:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:30:20 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 03 Apr 2026 17:30:22 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 03 Apr 2026 17:30:22 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 17:30:22 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:30:22 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:30:22 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 17:30:22 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 17:30:22 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 17:30:23 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 17:30:23 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 17:30:23 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 17:30:23 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 17:30:23 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 17:30:23 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 17:30:23 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 17:30:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d91612493fd72368b685c337f3f583067a94ee0ef306766e8d11839845e7daf8`  
		Last Modified: Fri, 03 Apr 2026 17:09:55 GMT  
		Size: 170.2 MB (170192316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7ddb9c49777c636a6c0269ee3791c6353c28422f751e0364954a9fd1cab295`  
		Last Modified: Fri, 03 Apr 2026 17:30:40 GMT  
		Size: 105.5 MB (105517571 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3db6efe217640858a1f1a6c8082966d3b890716465e0cc29b00e19cc4a7a28a3`  
		Last Modified: Fri, 03 Apr 2026 17:30:38 GMT  
		Size: 12.5 MB (12528429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d231ce9138869898f93c04f04de06b64cd08b5c4635307249f59fb25f4316b5d`  
		Last Modified: Fri, 03 Apr 2026 17:30:37 GMT  
		Size: 9.3 MB (9311182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b24c081e536927e9fdaa7d196be749a42470da491be9dbe2043ca34d2e05f01`  
		Last Modified: Fri, 03 Apr 2026 17:30:37 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71cbbeae7d8a6d6434abe619e913237dd69cb2abc0147b0a54f6e5d689649e6d`  
		Last Modified: Fri, 03 Apr 2026 17:30:39 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:393274974714c521e23b0c842917f06846cfa757d65b5152663e6e242a314a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:234b77d4ac321a115d6eed292894341b57bd149728f61833e7afb3d25484fcc6`

```dockerfile
```

-	Layers:
	-	`sha256:300335c91c35d45dc7e796535bb822acdd244a56b9e50338b0050688f9e4f810`  
		Last Modified: Fri, 03 Apr 2026 17:30:37 GMT  
		Size: 6.2 MB (6234509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80e6cf196b29cd488f548ee19b26f12c44b1667a8d2c65a7c40adc35833082f5`  
		Last Modified: Fri, 03 Apr 2026 17:30:37 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:a2a9a58b9212857e565450e965202af406a32124953487e660f74bd348c5ad64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.8 MB (347773553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0fab23efa1847840366325249d4638dfde32eb8024d71e68727d37138786cc3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:16:52 GMT
ARG version=21.0.10.7-1
# Fri, 03 Apr 2026 17:16:52 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:16:52 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:16:52 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:16:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 03 Apr 2026 17:36:26 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 03 Apr 2026 17:36:29 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 03 Apr 2026 17:36:29 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 03 Apr 2026 17:36:29 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:36:29 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 03 Apr 2026 17:36:29 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 03 Apr 2026 17:36:29 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 03 Apr 2026 17:36:29 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 03 Apr 2026 17:36:29 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 03 Apr 2026 17:36:29 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 03 Apr 2026 17:36:29 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 03 Apr 2026 17:36:29 GMT
ARG MAVEN_VERSION=3.9.14
# Fri, 03 Apr 2026 17:36:29 GMT
ARG USER_HOME_DIR=/root
# Fri, 03 Apr 2026 17:36:29 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 03 Apr 2026 17:36:29 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 03 Apr 2026 17:36:29 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1644240415892ae6adc3944665a6a99351819a4043adb69ab2e97d280a16aae6`  
		Last Modified: Fri, 03 Apr 2026 17:17:15 GMT  
		Size: 168.5 MB (168466722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c81367bc76e2cb7f5c28a1644228f827d98b08d3dfd73f3c61dfa047f5f098a2`  
		Last Modified: Fri, 03 Apr 2026 17:36:49 GMT  
		Size: 104.3 MB (104263411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:384ef9ae7e1a26ce46a1d2d7aed93dcac92c2570d6381275349eef5ccad19128`  
		Last Modified: Fri, 03 Apr 2026 17:36:47 GMT  
		Size: 12.8 MB (12789817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8f9c4fa1a2ee20c0a27261bbb1ff39299505a001c8a05c0e9135089863114a8`  
		Last Modified: Fri, 03 Apr 2026 17:36:47 GMT  
		Size: 9.3 MB (9311187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba297e682c1355d1cfd8f190001a3520d213a7f1b269f7cea964443d09837199`  
		Last Modified: Fri, 03 Apr 2026 17:36:46 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c6d69dec8cea830da732d97d5efb4e5efdee1906692b64e551d7114170fb365`  
		Last Modified: Fri, 03 Apr 2026 17:36:48 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:c7cfa2ee728286a3cf66d303daf03243c104ba8dcb6d9982373fa1d72e73a2e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754b6d7bb291036d0dde0f1da66d43c0a106024455c563fa7607b476f9605aad`

```dockerfile
```

-	Layers:
	-	`sha256:104df827c4a9225592d3f1d3888137d1cf712906a4a8b9c75a8efae3f3b7add9`  
		Last Modified: Fri, 03 Apr 2026 17:36:46 GMT  
		Size: 6.2 MB (6233442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44b1c1c59d521658ff273a6f0c92e7d4f565a8c98a73e46311b62e2a2ede997`  
		Last Modified: Fri, 03 Apr 2026 17:36:46 GMT  
		Size: 18.4 KB (18438 bytes)  
		MIME: application/vnd.in-toto+json
