## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:91c0e0b972ed8134ddc9b04fd8792af02303686faab51a9bff48d5eb0ae3aab0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:bc5446075a24e247d4ed18f7ec61456b88856e602b8e50099f3d4520094e58cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **523.8 MB (523848860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e7a91b518f987479f868a9aa8beafed765064e7598db2999e8a77983aec87`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:11 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:11:11 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:09:23 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:09:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:09:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:09:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:09:24 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:09:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:09:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:09:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7c2e3cf8908eccca20edf90d28e3fee070f14d8c192deedf6386f8c0d9b165a`  
		Last Modified: Tue, 09 Jun 2026 21:12:09 GMT  
		Size: 330.8 MB (330825369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e126eab08764eb633ddb20def8920b85369c2d98120da5848171f219298e989a`  
		Last Modified: Tue, 09 Jun 2026 22:10:01 GMT  
		Size: 123.7 MB (123652427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9ec14becc21b3a84f7908b1256f56ad274d075c91d4caac8da4464000ef49a`  
		Last Modified: Tue, 09 Jun 2026 22:09:58 GMT  
		Size: 5.4 MB (5438924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecd4369f3e2edb87063ceaf2cea708b02de5d36dd6c2718920a5e39fa8d36f6`  
		Last Modified: Tue, 09 Jun 2026 22:09:58 GMT  
		Size: 9.4 MB (9359973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61fb06b84efa5035e6ee6fd9d08ff36cfeb49affd10f33b1cbb3b3dd9ad162e6`  
		Last Modified: Tue, 09 Jun 2026 22:09:58 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4526c865c7fec0a337ca2ed7ab78d087d22c0a4455eec769a89d3901267ab4d`  
		Last Modified: Tue, 09 Jun 2026 22:09:59 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:9bee46b5f1ec55fb49d5cb0c99a2028460fa20b995015a8996d5b679732655be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850952 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe7fc1aae805b2e4710db13f755f6e754134ccf0eac3c2758e203a313c36d9da`

```dockerfile
```

-	Layers:
	-	`sha256:76ffa5ab189dcd2dd3213d6e1c3d99170f6abad0b2d033d9b43a881a0a7da161`  
		Last Modified: Tue, 09 Jun 2026 22:09:58 GMT  
		Size: 13.8 MB (13834667 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:211af6a5dea469961e026cfd34f1adad21240145e62822c84578ac03fd1acd6b`  
		Last Modified: Tue, 09 Jun 2026 22:09:57 GMT  
		Size: 16.3 KB (16285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:ad80dddf6c48099f64c0cbc02683a67b5c3357fdc59ddbe79d584ab8861c3975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **313.5 MB (313489795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934ef69ef671cc0eccc85e75b730672e8a97f5d9cce424a3ed2330021cead783`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:10:44 GMT
ARG version=1.8.0_492.b09-2
# Tue, 09 Jun 2026 21:10:44 GMT
# ARGS: version=1.8.0_492.b09-2
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:10:44 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:10:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 09 Jun 2026 22:10:44 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 09 Jun 2026 22:10:46 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 09 Jun 2026 22:10:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 09 Jun 2026 22:10:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:10:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 09 Jun 2026 22:10:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 09 Jun 2026 22:10:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 09 Jun 2026 22:10:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 09 Jun 2026 22:10:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 09 Jun 2026 22:10:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 09 Jun 2026 22:10:46 GMT
ARG USER_HOME_DIR=/root
# Tue, 09 Jun 2026 22:10:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 09 Jun 2026 22:10:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 09 Jun 2026 22:10:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac744debc1aeda7f8a15a7e95c01905f3886e894cc1989142c7256e5bc4cdaca`  
		Last Modified: Tue, 09 Jun 2026 21:11:04 GMT  
		Size: 118.0 MB (117955626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa876f4ecbffe8cf9ef7bf34c9e777ad1d9a12595e06c61184eb9462ff5745f6`  
		Last Modified: Tue, 09 Jun 2026 22:11:07 GMT  
		Size: 119.9 MB (119946114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7031949f19be56be8234d80fc67b65a8c61dad7ccdc7e84abf3dfe41ff412285`  
		Last Modified: Tue, 09 Jun 2026 22:11:04 GMT  
		Size: 12.8 MB (12769244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e03e550e45ff743456218c37abf7fe3013d6ee4e132a57fcf47975170f44c5f`  
		Last Modified: Tue, 09 Jun 2026 22:11:04 GMT  
		Size: 9.4 MB (9359970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb65e9ed0759f7899b9625f90d46fb511b88c41dea3c9652f29ebbbca22a49e8`  
		Last Modified: Tue, 09 Jun 2026 22:11:03 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9037744dbf5ab13bc624b67a51702a6c405601dd4fc82676fc33efe6dc90d34d`  
		Last Modified: Tue, 09 Jun 2026 22:11:04 GMT  
		Size: 161.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e51d49dac46593b9969df6659cceabf2b0312ab59f10bf9085c185fba7231f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04b525d09e221d4c3bb6c6e43171dd98031a7d9b2c1c0019f74797a1feef1fa7`

```dockerfile
```

-	Layers:
	-	`sha256:4a396a3774ecd7edca77214bf664bdc259988aa6bbfb977939f93b416faccf3b`  
		Last Modified: Tue, 09 Jun 2026 22:11:03 GMT  
		Size: 6.6 MB (6615976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b428f545fafccc76eb5fb536c318236342f77fb5dcc37cc668e1f4178d2ea0`  
		Last Modified: Tue, 09 Jun 2026 22:11:02 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
