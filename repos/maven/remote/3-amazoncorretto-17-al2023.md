## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:c00f7c06f537c347911974c81c1fa1fce67ac98df9db597be4e9fa69065be5da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:f1d3a0199c3f9bf576460c24c814a345d9ab19357ac443f489852117ff4ab8ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.8 MB (285764144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0ddf0c9078d81811866e8cd76cd3d24ddab77fc563e3799d78f08766927b495`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f9dd052e142d6bbee3556a17548362b00b044603d859f7ff1a81d3ef6d64bd6e`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 52.3 MB (52325199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f27b216893266cbcd2569d7245a76d6e97810526157ded6ed27143b7f9fe18d`  
		Last Modified: Sat, 07 Sep 2024 01:05:56 GMT  
		Size: 157.1 MB (157085615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01ad064beb47cc80377a7f3600eb8a5295c7116a073a3de01c9533de0814348a`  
		Last Modified: Sat, 07 Sep 2024 01:56:32 GMT  
		Size: 54.7 MB (54665688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b63732f21db098bcee3346ed4af7a3a5f44165504c17c6166c071b5ac931985`  
		Last Modified: Sat, 07 Sep 2024 01:56:31 GMT  
		Size: 12.5 MB (12516157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efe4f28c55a05f2df42e279c08e457a036a9c00e8b9a0f17e08f1c91a45765f6`  
		Last Modified: Sat, 07 Sep 2024 01:56:31 GMT  
		Size: 9.2 MB (9170442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69206f7a5528697ab8d14253654cceab6f4ea5d206627980944c5f2332de0dbb`  
		Last Modified: Sat, 07 Sep 2024 01:56:30 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43d405b2664e7e8fea98fd0ebf0b3449a91f2dc0b1d33305792da99a26074910`  
		Last Modified: Sat, 07 Sep 2024 01:56:31 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ee21b0b068fa573348dfeef8f4c17fa73a25a61a8c88771f0d253cff11df71e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6244191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb969d6c756454dabcd367631315df9b6ceabd3189e0ac2a6719b103a58bb2e`

```dockerfile
```

-	Layers:
	-	`sha256:3ab33b2c54d19c09ab04982635ce9c3429939cf3f23f1f698b632c0aa6f02821`  
		Last Modified: Sat, 07 Sep 2024 01:56:31 GMT  
		Size: 6.2 MB (6225908 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:234820fa3ebe964b34d2d9a5e034cdd763a57206f4aecbbe1a9062528500560a`  
		Last Modified: Sat, 07 Sep 2024 01:56:30 GMT  
		Size: 18.3 KB (18283 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:96b8eeab7762e6613145bfd352aeb22ac1eb68224fc9540ae92e40442214e58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.3 MB (283296126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fec94ebd5e41e92af942a87b65f7fe50368e44025065c552336a9d0c36ad2ed`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 19 Aug 2024 08:57:28 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 19 Aug 2024 08:57:28 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 19 Aug 2024 08:57:28 GMT
ARG USER_HOME_DIR=/root
# Mon, 19 Aug 2024 08:57:28 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 19 Aug 2024 08:57:28 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 19 Aug 2024 08:57:28 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5df0cce0a70b576e00cfe75d45089073c37754f2920c4a7a79f3ed6e6500982d`  
		Last Modified: Wed, 04 Sep 2024 22:37:28 GMT  
		Size: 51.4 MB (51426143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131d3188c2c6cdde0235867a7713fe8688b4158effa3ad76f093f085d3eb71b4`  
		Last Modified: Sat, 07 Sep 2024 13:19:45 GMT  
		Size: 155.8 MB (155786157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3f249089585d47203608271e5badad76b0b2f0d0fb52ade39059e8d2f613a3e`  
		Last Modified: Sat, 07 Sep 2024 14:55:11 GMT  
		Size: 54.1 MB (54123745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3928eab27892d51a0972af3a4440398447dc6750834e91581285324237956fd`  
		Last Modified: Sat, 07 Sep 2024 14:55:10 GMT  
		Size: 12.8 MB (12788599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b436ac992ad5f50818ca71bae3ceb05d392cc9ae7bd07bf47fea18a7754cbe4`  
		Last Modified: Sat, 07 Sep 2024 14:55:10 GMT  
		Size: 9.2 MB (9170441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fdcdbd2006dd920f445c4255ed654b6cb5bd78dbb37b54ab01637a1a699d5d4`  
		Last Modified: Sat, 07 Sep 2024 14:55:10 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f0043a85e62be188f1fc7804e44e902615325d50172c76d82af4335a7b322dc`  
		Last Modified: Sat, 07 Sep 2024 14:55:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:003026010a7783090bfe67a0776ada300f682407899d926cdd09ac258d79f27b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6243843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b67e79edd11ae5b9e82e92d907df0fb99c91d8bc4e6e786e3bccad79d89d1ae`

```dockerfile
```

-	Layers:
	-	`sha256:853b473d5bf0535abf1f608bb63c876e35026180448f1cd98573f104f86fd960`  
		Last Modified: Sat, 07 Sep 2024 14:55:10 GMT  
		Size: 6.2 MB (6224835 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f889fb05a2a4180a6e858364ee591889dce97bdd09e9d0d934950922ae27fe14`  
		Last Modified: Sat, 07 Sep 2024 14:55:09 GMT  
		Size: 19.0 KB (19008 bytes)  
		MIME: application/vnd.in-toto+json
