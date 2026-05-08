## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:1c43c25a974dcc5f02fb39bea30ba025fd215b562f8149fc7376ea6860de6d79
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:c8a824c287f1ec85a8f8f69ce07ce50190cd0edcae5e961b13fc47d763570e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **516.8 MB (516805926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e57b2cd5a240fc2344e9cbd0cd9b0752a1fc3c0965f82a2d35144ad0ecb8740e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:42 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:42 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:42 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 04 May 2026 20:45:23 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 04 May 2026 20:45:24 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 04 May 2026 20:45:24 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 04 May 2026 20:45:24 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:45:24 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 04 May 2026 20:45:24 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 04 May 2026 20:45:24 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 04 May 2026 20:45:24 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 04 May 2026 20:45:24 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 04 May 2026 20:45:24 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 04 May 2026 20:45:24 GMT
ARG USER_HOME_DIR=/root
# Mon, 04 May 2026 20:45:24 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 04 May 2026 20:45:24 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 04 May 2026 20:45:24 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cd2ff23a0524b1c7113ef94f2af3cff82ef1d7e86189b3e37a0a49a3e8a4e2c`  
		Last Modified: Mon, 04 May 2026 20:12:39 GMT  
		Size: 330.8 MB (330812379 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f41b57af2121ce2c9b4c834674ee89722fd9914edb4572dc4ca43d81419e577a`  
		Last Modified: Mon, 04 May 2026 20:45:52 GMT  
		Size: 116.7 MB (116657005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa55a1ec2085eaa092951f56bbcf8caca432845e8000b3d485560514506f3ecc`  
		Last Modified: Mon, 04 May 2026 20:45:49 GMT  
		Size: 5.4 MB (5446585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222083a7efebb67ef0dafc4540ccff990bc934f6ceba8bcf14146fdc57d22ee1`  
		Last Modified: Mon, 04 May 2026 20:45:50 GMT  
		Size: 9.3 MB (9312193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8aa9a080e031c8f27e329c871cdb43d999a4d18184153e903bb47e6f8e1221ee`  
		Last Modified: Mon, 04 May 2026 20:45:49 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9266be46ad927fbe2cfef001dcd5718ace79ec56e6b30aad420efec5540f44f`  
		Last Modified: Mon, 04 May 2026 20:45:50 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:87fc43881ffba08399eb9f0c7b458d75b977ae132d693fe200891c0f0a94d031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13850937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3c281a2647201cae0bc715cedc833e12a252e8b445a2ecd18bd0521289cf86`

```dockerfile
```

-	Layers:
	-	`sha256:743544efbd78c7a97473713e346c209ff12a41eb6af9cf82e92c622c474f7689`  
		Last Modified: Mon, 04 May 2026 20:45:50 GMT  
		Size: 13.8 MB (13834652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5e76143af6fcfa5da6cfc9d399102cc0ace2a1ffba2c4b9e9a4be46377bfb49`  
		Last Modified: Mon, 04 May 2026 20:45:49 GMT  
		Size: 16.3 KB (16285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:cb64a9ec14b9a067e683776c2abee767bcec89c8a2eb43707738b0f057ec0331
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.6 MB (306550589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67de3f4d61be98934612b4649fed5ee686d880e28bff6df950c909baf1b52663`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:11:02 GMT
ARG version=1.8.0_492.b09-1
# Mon, 04 May 2026 20:11:02 GMT
# ARGS: version=1.8.0_492.b09-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:11:02 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:11:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Fri, 08 May 2026 00:30:33 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 08 May 2026 00:30:35 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 08 May 2026 00:30:35 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 08 May 2026 00:30:35 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:35 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 08 May 2026 00:30:35 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 08 May 2026 00:30:35 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 08 May 2026 00:30:35 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 08 May 2026 00:30:35 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 08 May 2026 00:30:35 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 08 May 2026 00:30:35 GMT
ARG USER_HOME_DIR=/root
# Fri, 08 May 2026 00:30:35 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 08 May 2026 00:30:35 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 08 May 2026 00:30:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f663ff8f95b0ac33e5eeb3a57969767ad4ebbcf9ffbf6f56257306287e40928`  
		Last Modified: Mon, 04 May 2026 20:11:22 GMT  
		Size: 118.0 MB (117962667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9ded210afe29469c8467372322adc1280a2d1a74f1874dfba920242f7810da0`  
		Last Modified: Fri, 08 May 2026 00:30:56 GMT  
		Size: 113.0 MB (113045796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:082464239102037a6331cd91cdade2bca0132dd0607e4daa4a2a70a373b9303f`  
		Last Modified: Fri, 08 May 2026 00:30:54 GMT  
		Size: 12.8 MB (12772094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ae2c596c201f8618daf60920a809e866e6e9fb948feef328c36a4adcb98a31f`  
		Last Modified: Fri, 08 May 2026 00:30:54 GMT  
		Size: 9.3 MB (9312254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2a57fe6d339e708a8e472778432e064bd2ff08d8d398b23709efb3f5794072`  
		Last Modified: Fri, 08 May 2026 00:30:53 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f1eaa981b16364aebfa28f2581edefdb0436d36153f37cf2fe14ada3f4b533`  
		Last Modified: Fri, 08 May 2026 00:30:54 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:9f2d30d201c4a8ff9539374474635d4236c17f42edf6540e07606f03d34ad5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6632564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:472195213e3c6c0fe23ed4cc718ce1026772e3d77275915e040873115ea50100`

```dockerfile
```

-	Layers:
	-	`sha256:51aa1b82992580975cd43985c3a8844fd55eebc1476ba33ddda0776b4d725331`  
		Last Modified: Fri, 08 May 2026 00:30:53 GMT  
		Size: 6.6 MB (6615973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56f1c604b732f9186090ed41995290e57c455580c90b092a65d6891049015ece`  
		Last Modified: Fri, 08 May 2026 00:30:53 GMT  
		Size: 16.6 KB (16591 bytes)  
		MIME: application/vnd.in-toto+json
