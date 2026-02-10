## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:f7d41001d8011a76254a11f5c1a1ce3b0f998b2d4a9709b042957253cd568bd0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:983940ddcbe2701eeaec242522cac647f215379ac0e64ae042edf2c97e7ca03e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **330.8 MB (330759981 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5404b6b2725499b02c5b0e8028fb9639fcfd5c7373db0a1fcecfea45b4e66d7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:59 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:30:59 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:59 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 10 Feb 2026 19:09:43 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 10 Feb 2026 19:09:45 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 10 Feb 2026 19:09:45 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 10 Feb 2026 19:09:45 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:09:45 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:09:45 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 10 Feb 2026 19:09:45 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Feb 2026 19:09:45 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 10 Feb 2026 19:09:45 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 10 Feb 2026 19:09:45 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 10 Feb 2026 19:09:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 10 Feb 2026 19:09:46 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 10 Feb 2026 19:09:46 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Feb 2026 19:09:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Feb 2026 19:09:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Feb 2026 19:09:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4813123a6ec9537c4a8ad81d395a04d6cda2fb38203e651b03c910f6504f12a6`  
		Last Modified: Tue, 10 Feb 2026 18:31:19 GMT  
		Size: 153.4 MB (153363419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e6d45c1370b695f8e3d624673263ad7796c5ed2698e8468bf2b081bf2b67e11`  
		Last Modified: Tue, 10 Feb 2026 19:10:04 GMT  
		Size: 101.5 MB (101546600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84257eb4bc18f86a477521403618824d35f8127478fcb84843c6245b45ac199`  
		Last Modified: Tue, 10 Feb 2026 19:10:00 GMT  
		Size: 12.5 MB (12498451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b33197627dc351a19030475459f78df30836462746737e4cafe609e968f0828`  
		Last Modified: Tue, 10 Feb 2026 19:10:00 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f52e9d423abee775ba4e678df3974e47eab2c4644cd4b795533d8db0dc60ea3`  
		Last Modified: Tue, 10 Feb 2026 19:09:59 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f283924d7cb806b78ed4755a5697a1ea4fb3d62b50edc1ebfa995491e3b2fff`  
		Last Modified: Tue, 10 Feb 2026 19:10:01 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d2e26992b9733a16c21e3f7fd14d4f4a723d6187aac89b5482e73a1b770f9ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02b74b85c9e31ea19d5c7489979ec3796aea9247626ddedaf74a401159807b1d`

```dockerfile
```

-	Layers:
	-	`sha256:773c84fde5aab4e73f5ef3bf9252a2ed7fea3b5dc35be39e81568082585c457d`  
		Last Modified: Tue, 10 Feb 2026 19:10:00 GMT  
		Size: 6.3 MB (6257535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43338804bd4628fbcbb570323d4533f271af50c789252303ecda477e6e7c43f1`  
		Last Modified: Tue, 10 Feb 2026 19:09:59 GMT  
		Size: 18.3 KB (18291 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:059483908816b4f5cd8b1ab5c030c91a9d0652d653e7d54c35d6c6f442c01b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.3 MB (327289323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d89cba2229383f2ba18bb8ea841c283fe06c2a35b36a63d0063309a5810b89a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:51 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:30:51 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:51 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 10 Feb 2026 19:12:14 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 10 Feb 2026 19:12:16 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 10 Feb 2026 19:12:16 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 10 Feb 2026 19:12:16 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:12:16 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 10 Feb 2026 19:12:16 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 10 Feb 2026 19:12:16 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 10 Feb 2026 19:12:16 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 10 Feb 2026 19:12:16 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 10 Feb 2026 19:12:17 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 10 Feb 2026 19:12:17 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 10 Feb 2026 19:12:17 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 10 Feb 2026 19:12:17 GMT
ARG USER_HOME_DIR=/root
# Tue, 10 Feb 2026 19:12:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 10 Feb 2026 19:12:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 10 Feb 2026 19:12:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe09cbb5e7a2b065a6b8b1308384deff3a73a806922a2cad78f5af69f4a16aff`  
		Last Modified: Tue, 10 Feb 2026 18:31:13 GMT  
		Size: 151.9 MB (151920991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9dcaac6fb9aa413f5ca9cd50cdb1a21d1812b8ec3c687fb07c89575eb78180d`  
		Last Modified: Tue, 10 Feb 2026 19:12:35 GMT  
		Size: 100.4 MB (100379499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74171fbdd0870269b9e986c0d69cf53a7332cec9269ad36bf12909e0cf93fea7`  
		Last Modified: Tue, 10 Feb 2026 19:12:33 GMT  
		Size: 12.8 MB (12757335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a78981aca41255d35a868e0fd84238408a505d1bd81307df85eb21b606549622`  
		Last Modified: Tue, 10 Feb 2026 19:12:33 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a588b926cc94f98a5583f524acbd0ccce049e0733f6fb999b78c588961c3a6`  
		Last Modified: Tue, 10 Feb 2026 19:12:32 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f189223ff37420f76460df4de99ce934985b98e50c408f603940060ea6b7f3bf`  
		Last Modified: Tue, 10 Feb 2026 19:12:33 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ae38e44846d1ded34721287cabd0e4a41c6dcae38a3c1be1bc85fb7b874486dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58f76c7ba3595916c35c089b6aaafdbd7710a757042656c7bb67519223b1c482`

```dockerfile
```

-	Layers:
	-	`sha256:2a17b630f8fc3d5b0381c0cb7669b9dfe3ec7fbb928072929434767f28baa708`  
		Last Modified: Tue, 10 Feb 2026 19:12:32 GMT  
		Size: 6.3 MB (6257309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aba3f0437486adbd8baa36f6880c2e49cc73d6241fcb32cca4b79ee805b37723`  
		Last Modified: Tue, 10 Feb 2026 19:12:32 GMT  
		Size: 18.4 KB (18439 bytes)  
		MIME: application/vnd.in-toto+json
