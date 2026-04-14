## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:11413c52165fe52d266638e5c8e1e0bf0a6a78fa8930ce0463578d410f0cb4b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5c0731930c1fca3477f349422e370d631e9e0829bee38809220a273fcd1735f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342383623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cfecf457e1d29531ca95c64f000e8e362dfb8af8cee7d1bf38ed3d24122237`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:28 GMT
ARG version=17.0.18.9-1
# Mon, 13 Apr 2026 22:48:28 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:48:28 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:48:28 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 13 Apr 2026 23:42:46 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 13 Apr 2026 23:42:49 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:42:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:42:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:42:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:42:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:42:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:42:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:42:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:42:49 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:42:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:42:49 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:42:49 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:42:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:42:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:42:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:528f2d457822761b2ba8bc1e5efc67990ba22804d685a53272e53c42948a0125`  
		Last Modified: Mon, 13 Apr 2026 22:48:48 GMT  
		Size: 156.9 MB (156911250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6d7e331893a5260ffba07b55e7c5036fa5c0cf627cec75d1c9c27c0641cfbe5`  
		Last Modified: Mon, 13 Apr 2026 23:43:06 GMT  
		Size: 109.1 MB (109056752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6575f0ae251feefdf41b0dcf390dca619d62874340be95fe53b803c90391a03d`  
		Last Modified: Mon, 13 Apr 2026 23:43:04 GMT  
		Size: 12.5 MB (12532149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4362f88b873bc6982e857338ccc34c29d0ee79235f4ba2865bb76332f272e0eb`  
		Last Modified: Mon, 13 Apr 2026 23:43:04 GMT  
		Size: 9.3 MB (9311177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97365b9db2f740f07c613c207f27ce30a99c0567c56f0b9c3ab66fc00458442f`  
		Last Modified: Mon, 13 Apr 2026 23:43:03 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed51e79107ce3608cd0c7209bae6322674cb82feb1e6431b7e973317f223caa8`  
		Last Modified: Mon, 13 Apr 2026 23:43:04 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:58e56ea06a3b6e942d863fe50100deac4c58e897daff86cee8f1992c8e7b2c71
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6256748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd77aa10a435a8f40396813aef644460a7bc32f156bd7619eb6fcb8dd38b3cc2`

```dockerfile
```

-	Layers:
	-	`sha256:89cf29365655e291f54ba7354d221b68d30468892493abdba6c97a9f2ea33d08`  
		Last Modified: Mon, 13 Apr 2026 23:43:03 GMT  
		Size: 6.2 MB (6238457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:51ff3a14d1399e162086b0bca10b80526342f8bd36fde92e0a83c9c691b93690`  
		Last Modified: Mon, 13 Apr 2026 23:43:03 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:49bf6b9b1b5dbe3955170bfc498340761d9bdba0e41c71cacc364650fa2ea5ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339176658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26cdf8975ac15e0c4056451c25cd5256b289b9f6f75db2321e5f9060e03b7cef`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:11:22 GMT
ARG version=17.0.18.9-1
# Mon, 13 Apr 2026 23:11:22 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:11:22 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:11:22 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:11:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 13 Apr 2026 23:56:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 13 Apr 2026 23:56:17 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:56:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:56:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:56:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:56:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:56:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:56:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:56:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:56:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:56:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:56:18 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:56:18 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:56:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:56:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:56:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:011f49c7a752bcb4f2e4bc4e48d4c5985fcab3bee94df2d87c4db7e96131efd0`  
		Last Modified: Mon, 13 Apr 2026 23:11:45 GMT  
		Size: 155.7 MB (155728187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c915cdc8c1c7ccd278995b85eeb91c690a90702bff39e3b7cc85e853999bd6f8`  
		Last Modified: Mon, 13 Apr 2026 23:56:36 GMT  
		Size: 107.9 MB (107903484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca0c0526645e147b8b5c75db988a8d6b56275d145fa5f53202267857206f25e`  
		Last Modified: Mon, 13 Apr 2026 23:56:34 GMT  
		Size: 12.8 MB (12790033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f4d7519fb562ecfca6392793dcbbe1a9de29aa7661d7ad1f0ed583245776f0e`  
		Last Modified: Mon, 13 Apr 2026 23:56:34 GMT  
		Size: 9.3 MB (9311175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f594b60e35cd7496241f13bf8fb0aed1d1dea8e8b1cde206ba4a41c05922d5b9`  
		Last Modified: Mon, 13 Apr 2026 23:56:33 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:142f8a71f5a8bb848c0ef91245794007c252a191d1bacfa6536728765e03223b`  
		Last Modified: Mon, 13 Apr 2026 23:56:35 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:59bb1f1024c62f41bb8e77b40e89f7a3600e61aea49946d92f3538205ef9a74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6255826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b86fcd5b1d8815356a20be6f067d55fa540cbc73fd980e366a3f8f06b962ce8`

```dockerfile
```

-	Layers:
	-	`sha256:91df34169f9f6200fb26edcf54972fa3162a4dc6c300fe13db62a5727042aa62`  
		Last Modified: Mon, 13 Apr 2026 23:56:34 GMT  
		Size: 6.2 MB (6237387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc68be16b1c98427bd2870d336029a4181e710310d85b362535489bb09a2b538`  
		Last Modified: Mon, 13 Apr 2026 23:56:34 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
