## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:c6fc64680b07b57c3df3137319c27f0619da7e36213b7a169472c07f59f47495
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:b02d36197835227f1f01c0e0bfca2cc83a6c1d687d1def42c2deb568e63b3491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.9 MB (497920463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c103ba5c0d8e2099a84c4aa74b3b09eb42e3e3224eef23ecff9c81b421e13b5b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:42 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:42 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:42 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 17 Dec 2025 20:09:33 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 17 Dec 2025 20:09:33 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:09:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:09:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:09:34 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:09:34 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:09:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:09:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:09:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56aa5671e4c6388bab5eaf668041a81c0906c37489a66a044c651a8ef17681b4`  
		Last Modified: Thu, 11 Dec 2025 22:12:45 GMT  
		Size: 330.9 MB (330888100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:787e12f7089364c92856736823e8ae672a58d3f26993814685c94f5eb05d9a6e`  
		Last Modified: Wed, 17 Dec 2025 20:10:25 GMT  
		Size: 98.3 MB (98312512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9715db448a1131b227f5fa70f569d3cd449258d26d77dde50a4412fe5703022`  
		Last Modified: Wed, 17 Dec 2025 20:10:11 GMT  
		Size: 5.4 MB (5418107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef48b859eb1108109c3f19186cf1de7b6b87ff62fbca6f02aeaf388aaf855d8`  
		Last Modified: Wed, 17 Dec 2025 20:10:11 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fa8a2a8063666d8fb18c72534e0a948e2096b1df02e335aa9c5bc29417f8f84`  
		Last Modified: Wed, 17 Dec 2025 20:10:10 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d234c86a02aeb369c7c2693705fc3d1bb1e4b5b44cd273be1a827525c1142456`  
		Last Modified: Wed, 17 Dec 2025 20:10:10 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:64c3a4d53d217277441b229327f57df89214cd3e7ee56e73263685ea288639eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.8 MB (13846492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:baf28e6eae08c0196f2d665c3cf495f8cc20bf7a298f1b0b3e8ef13dba5cb122`

```dockerfile
```

-	Layers:
	-	`sha256:f807dbf57960ae646095ac0e918ad45203abb469d9577fe16cd0b8288d7db5a4`  
		Last Modified: Wed, 17 Dec 2025 21:30:21 GMT  
		Size: 13.8 MB (13828216 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14021fce14f183b8caf8b6b2db0db1db8bff9edec7d68aee5dcf95c31a02313b`  
		Last Modified: Wed, 17 Dec 2025 21:30:22 GMT  
		Size: 18.3 KB (18276 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:63887bad3f524734a6fe2cd9323d5710c097fe8b935eb3ad60dd9a1887e11ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.8 MB (287829779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20e7a6cda216e533b22cfb63818ca31296d5dc1b191d3c3221274a20902d1e11`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:11:30 GMT
ARG version=1.8.0_472.b08-1
# Thu, 11 Dec 2025 22:11:30 GMT
# ARGS: version=1.8.0_472.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:11:30 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:11:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Wed, 17 Dec 2025 20:09:18 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 17 Dec 2025 20:09:20 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 17 Dec 2025 20:09:21 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:09:21 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:21 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:21 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:09:21 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:09:21 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:09:21 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:09:21 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:09:21 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:09:21 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:09:21 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:09:21 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:09:21 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:09:21 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c48e9835d76eae2b2c4e9d6c02f6408efc2e56451c92c8fa9e4c21b8dd8690`  
		Last Modified: Thu, 11 Dec 2025 22:12:13 GMT  
		Size: 117.9 MB (117927059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e691b4596dbcfa94c7d035832fee7e28ec20225a241894bbfad24ac91f837618`  
		Last Modified: Wed, 17 Dec 2025 20:10:12 GMT  
		Size: 95.0 MB (94986190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a3d4570068352e179a62511350e4620d6420a3d8982c2cabbf1d904f4919889`  
		Last Modified: Wed, 17 Dec 2025 20:09:49 GMT  
		Size: 12.7 MB (12729795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1034073e538d1149c932e3d314ca9b683f4dcd6d45bb9eb294336aa4e676752`  
		Last Modified: Wed, 17 Dec 2025 20:09:49 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77064ab1b5c31b11056779da48c49bfb0e1efd396f67dd10030bb230427a5b06`  
		Last Modified: Wed, 17 Dec 2025 20:09:48 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299a7429e8396725afeed80b84fe2fb4d4ae69334a473d4cc5f79f555cac35ba`  
		Last Modified: Wed, 17 Dec 2025 20:09:52 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1e703ebd5a1735df8e75231e0b1af5af8efe525f62b764dacc46c91d535aed9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc75f40fd5e82bee7ca2f632fee19eca40050878af91bc84cd2ddba048df4ef`

```dockerfile
```

-	Layers:
	-	`sha256:6c0254b99c9120cc177b370054ff98ad8d07dea20a1eb1b95236adba8ce90f50`  
		Last Modified: Wed, 17 Dec 2025 21:30:33 GMT  
		Size: 6.6 MB (6609537 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc523b36081e27b150b8e94eabf3e1283fcb1baa2c214199186bbb63d9095d82`  
		Last Modified: Wed, 17 Dec 2025 21:30:34 GMT  
		Size: 18.4 KB (18428 bytes)  
		MIME: application/vnd.in-toto+json
