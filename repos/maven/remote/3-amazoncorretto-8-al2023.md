## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:756e0694a52ad3c4507115ec54aa4263518de88f5aec905fc11fd7c16f7497ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:e207faa290670d386ca0b4e4fecbeca39eda09e2da2e113b4a5ad8026813130a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **414.4 MB (414404806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6530aabf6014194fd2a28f9c5f8fc2a6ddfcdb049831113a849427e2b004451`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_442.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8edd281e9a4ac0b8fff33aec76d28cdd12f739df5f75cf92c9ba6ac284a82891`  
		Last Modified: Thu, 23 Jan 2025 18:28:21 GMT  
		Size: 285.7 MB (285705648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e351eaeeaafbb78e2df79cdc0e50333e2b0233a140bb1fd6e989831dc4e9d66`  
		Last Modified: Thu, 23 Jan 2025 19:28:20 GMT  
		Size: 61.6 MB (61586366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c123a6d3661da88db23069885ed371066eef533f066307e88536cfce8806ce1`  
		Last Modified: Thu, 23 Jan 2025 19:28:19 GMT  
		Size: 4.8 MB (4790845 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e60be37ca73bd7ba72c06e1b6444cb152c9ba8c881ce61fdb3b3ce8a673ac4`  
		Last Modified: Thu, 23 Jan 2025 19:28:20 GMT  
		Size: 9.2 MB (9170429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ff178a111666e3e052e2056b648c93f5e243cb91399f0499ac1e5346e1e195`  
		Last Modified: Thu, 23 Jan 2025 19:28:19 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce988a2ff0141c8432f78776f223247b7717621797be5c78c31312c7630b2ad`  
		Last Modified: Thu, 23 Jan 2025 19:28:20 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:890e9f5c346ba4a67106ee97c195e2424652b63e294fcb8a766b3b8c73309501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.7 MB (12718733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:124cc9b62923139f6332b97ce19d359e694230ec6f1fc1730581d2e29fac0103`

```dockerfile
```

-	Layers:
	-	`sha256:3b0565fb42842acb184de030e3fa4be5ab6619ceddffc1860bd31b1cc4aca7b5`  
		Last Modified: Thu, 23 Jan 2025 19:28:19 GMT  
		Size: 12.7 MB (12700422 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d165a32490e49f026c37f07489691659d2003859490cc78dd469c26900f72fba`  
		Last Modified: Thu, 23 Jan 2025 19:28:19 GMT  
		Size: 18.3 KB (18311 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:22494b66bc061a8fcfcba078ef5b25b4363538b2310627097c75fbb67fa7f562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.5 MB (252482962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1b26cf4a6797f387ca5e8701e337b44a07bc62008599a5546ce8f9acd2b3f8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /rootfs/ / # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/bash"]
# Tue, 20 Aug 2024 18:12:59 GMT
ARG version=1.8.0_442.b06-1
# Tue, 20 Aug 2024 18:12:59 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=C.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37f32f5975391f609169f0b280e968205c77f19493b604fd8c6ad3481ebf1fd6`  
		Last Modified: Thu, 23 Jan 2025 18:29:47 GMT  
		Size: 118.7 MB (118695959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cadde126c5b8bb0c4a3023176ff47484c0c74c84b4c4a9ffcb6a2b33975967`  
		Last Modified: Thu, 23 Jan 2025 20:03:13 GMT  
		Size: 59.6 MB (59557246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e122324ec3a09dfd259530a5b2a5a0a80c0318f96b1048991b4b014c1603910c`  
		Last Modified: Thu, 23 Jan 2025 20:03:12 GMT  
		Size: 12.8 MB (12790080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b37cb04a7aaf98fbdd21b8a98613a324e1fd63db60d4d73ba157356e8437ea1b`  
		Last Modified: Thu, 23 Jan 2025 20:03:12 GMT  
		Size: 9.2 MB (9170435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c8f9b3e1286e1ec8ba18e661c9e7dcf2cdc174be23d19178b1760b2597edee`  
		Last Modified: Thu, 23 Jan 2025 20:03:15 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea190e49d07eb30b88dec46f63d24081ed0587dc366cc76bb9c281e6caa7452e`  
		Last Modified: Thu, 23 Jan 2025 20:03:19 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:6bb6b3afe77a00265c0f95eca7ae45eb6970a51252960930eadeb7ccdd9d7bf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6619804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc94b2ca3a9f1d510213eb29218e4d9871517533263a5c71f688802781f82e8`

```dockerfile
```

-	Layers:
	-	`sha256:b79a1302a3be6d060fb6bf993c411f67f2bb0a581e12e8ddc192186ebb575e23`  
		Last Modified: Thu, 23 Jan 2025 20:03:10 GMT  
		Size: 6.6 MB (6601339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:973d78be7bf73e4262a0eb70c07cf7d556a7c9562e1e05ee97f5f37f68d905ac`  
		Last Modified: Thu, 23 Jan 2025 20:03:10 GMT  
		Size: 18.5 KB (18465 bytes)  
		MIME: application/vnd.in-toto+json
