## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:aebb67356d924c52908878db1398007f0ea6d7aff6a3ff76077f9e34f39c4547
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:190a86c4bad4ac17430f2730fa4374f1f6b26438264ea21fe58fa16aa906331c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **317.2 MB (317184411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5da49801b66260e8adc4e36cf173fd795329d086f926ecd26619bbb16969a9c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de13c20e9df957b6be83fcb1f3c53226c48d2120ff5c540a20c7d58c051af08a`  
		Last Modified: Mon, 25 Aug 2025 20:54:55 GMT  
		Size: 156.8 MB (156792554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0544bdf288e78e0137b619ad3f3850e293bd3737dc75fbf8a15460b0feddf264`  
		Last Modified: Mon, 25 Aug 2025 23:31:33 GMT  
		Size: 84.8 MB (84767650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c668fdf7179f6dbfff40ea05caa937eb56dd53c97e3c615b8877ef952c1ec7b`  
		Last Modified: Mon, 25 Aug 2025 20:56:01 GMT  
		Size: 12.5 MB (12511851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9afb8e3421b2d82adba8a984d90b41fb738fbc3cc5e069801c3ac4f965e032ec`  
		Last Modified: Mon, 25 Aug 2025 20:56:01 GMT  
		Size: 9.2 MB (9242583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78289a701572570fd1f72a16f54d4ddbfaa92aa72df3c8e759b4ef2898a43ade`  
		Last Modified: Mon, 25 Aug 2025 20:56:00 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d67468ffed6a3aeb44761fc28a86cf3dc8c26f0250fba515b9f5f56f7fc788a7`  
		Last Modified: Mon, 25 Aug 2025 20:56:00 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:11bc53dd4b9871f06721e2ae3a43cf3951d92b71eeb995ccef8fcd1ad44a4b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a469c6d8ae3a3d1747371007849cf4ead59a1966e263b6d76b37dd9224c13b2`

```dockerfile
```

-	Layers:
	-	`sha256:69511fd762ba98a101c067197c23c61d5fdc803e998cbf4c6153292719e877d8`  
		Last Modified: Mon, 25 Aug 2025 23:27:38 GMT  
		Size: 6.2 MB (6231938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc557099b95e1f8a0be1b0a27e05383471f55674d52f6979e8eb2ee03789f942`  
		Last Modified: Mon, 25 Aug 2025 23:27:39 GMT  
		Size: 18.3 KB (18328 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f2d80ba40474377bd4f84fb88b98661aec37998d4e080e3fa036761a32d01ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.3 MB (314260142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f07f4df9a0469884835f49c2c735d6e0ddb8e3013c07de0d5977635688dbf7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["/bin/bash"]
# Wed, 16 Jul 2025 06:51:38 GMT
ARG version=17.0.16.8-1
# Wed, 16 Jul 2025 06:51:38 GMT
ARG package_version=1
# Wed, 16 Jul 2025 06:51:38 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 06:51:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN yum install -y openssh-clients # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 16 Jul 2025 06:51:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 16 Jul 2025 06:51:38 GMT
ARG MAVEN_VERSION=3.9.11
# Wed, 16 Jul 2025 06:51:38 GMT
ARG USER_HOME_DIR=/root
# Wed, 16 Jul 2025 06:51:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 16 Jul 2025 06:51:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 16 Jul 2025 06:51:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f0b7d54214a6f9c2c7698f71fb06f2128097c3f9d97269e3d449f7639c142381`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 52.8 MB (52768497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39038ba68b49b780e3534ccce1b6b6272c306e317dd4edea7619d07af966f6a0`  
		Last Modified: Tue, 26 Aug 2025 00:09:53 GMT  
		Size: 155.6 MB (155582265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153bb2d439d8441912bcdd1b390ac3e12e46a3cb46486521581a94ed4bfee3ad`  
		Last Modified: Mon, 25 Aug 2025 23:38:10 GMT  
		Size: 83.9 MB (83895078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4371cce339ae8319b085cb799913e7929013c5b5dd87e007aacd5eca5b601c0a`  
		Last Modified: Mon, 25 Aug 2025 23:37:54 GMT  
		Size: 12.8 MB (12770669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e3da3199bc01888e8b165712cee233f538f09149b5e96a922031f5380e7e55`  
		Last Modified: Mon, 25 Aug 2025 23:37:55 GMT  
		Size: 9.2 MB (9242588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:778f14902b7de58dca02496884f2f2b593c5660c1cc88168dc0b5f59214def30`  
		Last Modified: Mon, 25 Aug 2025 23:37:54 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc17a8ef8fdde17962850796d5925cf5836cbf90690555d3ff63d1e49e721fb`  
		Last Modified: Mon, 25 Aug 2025 23:37:54 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:bbbbd8bb616d1d8e955164fa3546d52fe81e92a3d1dcae707905f78559502cde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6663554189c69c845ce6ccbccc6e797aad56c3959082f07bd35299bb363dbe0`

```dockerfile
```

-	Layers:
	-	`sha256:40786df94740df7089bfa0514c4797624bc2c6a32bfdd69a3a052e2afe4d7e5b`  
		Last Modified: Tue, 26 Aug 2025 02:27:46 GMT  
		Size: 6.2 MB (6230868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59799a86d0f242c006f4d88a77aa9c4b8b10e4714dbcce22d61c9050cc40ae81`  
		Last Modified: Tue, 26 Aug 2025 02:27:47 GMT  
		Size: 18.5 KB (18476 bytes)  
		MIME: application/vnd.in-toto+json
