## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:92db90a8f41421c2c4a601e43f7f2f90244102a192d240ea576d4516f7ce54b5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:8d70690e80bcf0cf3d5a3b2a81ced376f8dd1f57002a742171a9ae87d7dd4e59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.3 MB (320326296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a0eeb8497dabf68c5a779540c3ab8d946539404d7a510551a112bf14a382b35`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b98c9726d5df7bed3c459752d2d5d55f490e81108e14191e990cc699ea251a3`  
		Last Modified: Fri, 13 Jun 2025 17:12:40 GMT  
		Size: 169.8 MB (169841421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83a01aaef095bf5e54f7bebaa4f2f3075d62ea128354b9f8603605adde5da7d`  
		Last Modified: Mon, 23 Jun 2025 17:31:35 GMT  
		Size: 75.4 MB (75420389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1471834b0f8ad9a74be7744f00039095b1f146c20e55a6e36d23ed2d7394ff`  
		Last Modified: Mon, 23 Jun 2025 17:31:16 GMT  
		Size: 12.5 MB (12539681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f984e4a4dea7649c99623751623c5e2e1c010160a6f791b7ee7ab72f16866683`  
		Last Modified: Mon, 23 Jun 2025 17:31:15 GMT  
		Size: 9.0 MB (8953405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:306bcdca187528ab2030aa3ae1050f27d7c48afd0250e04378a2a801dd5eb493`  
		Last Modified: Mon, 23 Jun 2025 17:31:14 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c35607eb202fbf7c34aa464d2ef4214daa96e83d25cbdcb5916bd404f791ecb`  
		Last Modified: Mon, 23 Jun 2025 17:31:14 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:c336d42beaf2956a13273ca542c5c4f0626ec2bd73432327f1124beee593d28d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e55038ead866a59ba20dcef11205296ca3f617187ed2e887519fc4c51a175f42`

```dockerfile
```

-	Layers:
	-	`sha256:16b2f8870ebf3ea2d248ab27e5557f03e9a48ad302d092b9f761439651a021da`  
		Last Modified: Mon, 23 Jun 2025 20:28:49 GMT  
		Size: 6.2 MB (6232494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:670667b1b4e21c504aa4361f0546a63b64ded24d6b15019f0dfaf6194c6ba1b6`  
		Last Modified: Mon, 23 Jun 2025 20:28:49 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:7f70bf6382de8a851514ccc6f830602669a82c265cf9bd5599e40f37268a92df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **316.9 MB (316944704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b264b5778b033f0abbcb97fd2cb70f22a5da0180cd1bf9d75a8766b3a851198`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=21.0.7.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN yum install -y openssh-clients # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sun, 22 Jun 2025 10:21:55 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sun, 22 Jun 2025 10:21:55 GMT
ARG MAVEN_VERSION=3.9.10
# Sun, 22 Jun 2025 10:21:55 GMT
ARG USER_HOME_DIR=/root
# Sun, 22 Jun 2025 10:21:55 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sun, 22 Jun 2025 10:21:55 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sun, 22 Jun 2025 10:21:55 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ff4b3666dea278d1d6ddf7a32dd123f036a63f55353610d3938a9a84bcf3c2`  
		Last Modified: Fri, 13 Jun 2025 21:51:27 GMT  
		Size: 168.1 MB (168143613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ebf35dd71db1ab58cb24b8b9f1415b03615a1afdfb10fff1c69302b69ce3224`  
		Last Modified: Fri, 13 Jun 2025 21:25:23 GMT  
		Size: 74.5 MB (74542749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39ec470fafc99284edde4b97c81af6b9c90e1ee41b529d7285dcf935fe93a8dc`  
		Last Modified: Fri, 13 Jun 2025 21:25:19 GMT  
		Size: 12.8 MB (12822212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:395c8203d82b1b0d9e46474444e16bb7bd09c0a97881127710edb14e7127f479`  
		Last Modified: Mon, 23 Jun 2025 17:44:08 GMT  
		Size: 9.0 MB (8953403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e20cc2048605c12a6f998eb2486b8b6c861dea2bd7ecad44d35d8c984ef2df56`  
		Last Modified: Mon, 23 Jun 2025 17:44:07 GMT  
		Size: 847.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc472065053e7495421e1c472df32ed3921602054448a179b72d8efbda1cd4c1`  
		Last Modified: Mon, 23 Jun 2025 17:44:08 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:197aa8b0621b2ba9fd38f54cf943930156cd2b1a21c9b7da977620e6341d93ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5b84aa9ec2bfeee842a8e71f76ed3ae591f1e73bd136040c35670552d481069`

```dockerfile
```

-	Layers:
	-	`sha256:30203ecba1fd1b86fd58f8a04c7b3ed2ca93388e84bd32d0197d4d3a014e7671`  
		Last Modified: Mon, 23 Jun 2025 20:28:55 GMT  
		Size: 6.2 MB (6231427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7caa91c4fd363bfafe378c53cfdad6e61925f2dcca60f7f837162314bef3251`  
		Last Modified: Mon, 23 Jun 2025 20:28:56 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json
