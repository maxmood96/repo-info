## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:17c8226cb8ef170d69a8e0b3e67bdb790b87952a8b048f9098e121cb07280c36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:59d740a5a757f80bda8d653c70e57b53ea8ed95c186e660cc8b8a5cafb9e9235
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.9 MB (354854770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f977039dc343563743da1b9bca2761837841bb3089f4a90caa366dd5d0adfac6`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:37 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 23:12:37 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:37 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:37 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Sat, 08 Nov 2025 19:24:14 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 08 Nov 2025 19:24:14 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:24:14 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:14 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:24:14 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:24:14 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:24:14 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:24:14 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:24:14 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:24:14 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:24:14 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:24:14 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:24:14 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:24:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:24:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ff4d7205da8b8271c826b4d33c535dc537a1d647dc5aaac7acbed9389cdd36`  
		Last Modified: Fri, 07 Nov 2025 00:11:33 GMT  
		Size: 189.2 MB (189168050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a394463826ec7467413583d92a73c4896742f4816f216dece19805e86d4e996`  
		Last Modified: Sat, 08 Nov 2025 19:24:33 GMT  
		Size: 102.4 MB (102442599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7793b4f6b80a563b946690bffe17edc133d5dc1b69fd6b839d47fe0799b9d054`  
		Last Modified: Sat, 08 Nov 2025 19:24:39 GMT  
		Size: 9.2 MB (9242577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:170bf6d393b05acc80d2f927b5c36a6b2c9ee958512b7a76d267873fce1b239e`  
		Last Modified: Sat, 08 Nov 2025 19:24:39 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ea11eb817aefaea5e066357524bda83d4877da6ded0b60746794876a315317a`  
		Last Modified: Sat, 08 Nov 2025 19:24:39 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:78ba9a9f358e3d5489a68d3e2f88d72143d6ebb9c7b2fc37a4ee672b8515c993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba6df5c88e52ce55996ced2a26dd65a342668df2be5f4a83516a12b334c9cd1`

```dockerfile
```

-	Layers:
	-	`sha256:4d200088d91717d0cdc997f91cb035af64f077244f61e89077dd6701b21cb293`  
		Last Modified: Sat, 08 Nov 2025 21:29:35 GMT  
		Size: 6.2 MB (6207774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bda5049b4c23da70872fb1041c34932707fac57e8fcb1725c852003da05a369`  
		Last Modified: Sat, 08 Nov 2025 21:29:36 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:47ba09d5f8d565006c957e798a614a9a10c8e1be42705c6d40394df18e1028ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **351.0 MB (350989463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9fb1ec52bbe4e90ce3c48b05aaf4dd42266ad6de652373c959ca377111df796`
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
# Sat, 08 Nov 2025 19:23:53 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Sat, 08 Nov 2025 19:23:54 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Sat, 08 Nov 2025 19:23:54 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:23:54 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Sat, 08 Nov 2025 19:23:54 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Sat, 08 Nov 2025 19:23:54 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 08 Nov 2025 19:23:54 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Sat, 08 Nov 2025 19:23:54 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Sat, 08 Nov 2025 19:23:54 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Sat, 08 Nov 2025 19:23:54 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Sat, 08 Nov 2025 19:23:54 GMT
ARG MAVEN_VERSION=3.9.11
# Sat, 08 Nov 2025 19:23:54 GMT
ARG USER_HOME_DIR=/root
# Sat, 08 Nov 2025 19:23:54 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 08 Nov 2025 19:23:54 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 08 Nov 2025 19:23:54 GMT
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
	-	`sha256:06308752fab60ebab35469070a607983275728612ba715f1e0f52099fa6cc39d`  
		Last Modified: Sat, 08 Nov 2025 19:24:33 GMT  
		Size: 101.8 MB (101751755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2357018c4839e5be2efc7463d996c8061e04ef82b9d17bba373be5b9ba459d42`  
		Last Modified: Sat, 08 Nov 2025 19:24:20 GMT  
		Size: 9.2 MB (9242576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f15552c04f50b8948a2ec49214862faaa53d422aaa3f1cf584874c64b9446bd8`  
		Last Modified: Sat, 08 Nov 2025 19:24:20 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a25e0fac9ea4a6b375e1892ea8e2856d145bcf43f973ed68fc6b51944725a1f5`  
		Last Modified: Sat, 08 Nov 2025 19:24:20 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:7434217cfc131178523802f163d19d23a4a58ae7cee8ea5e6e467f64741294e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134f973663ab534f2c23242d903986a483493e0ac81e50b2ba04efee17a7ff4a`

```dockerfile
```

-	Layers:
	-	`sha256:716d772cfb56b3afae7f54eeeaa371c35ceef285c318e96e379594f7ba4d7942`  
		Last Modified: Sat, 08 Nov 2025 21:29:41 GMT  
		Size: 6.2 MB (6206718 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0383e98deb013088a3fb2af78a468808dfbbbf83cabf62bf6cc3d9c207e02d37`  
		Last Modified: Sat, 08 Nov 2025 21:29:42 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
