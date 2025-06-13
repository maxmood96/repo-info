## `maven:3-amazoncorretto-24`

```console
$ docker pull maven@sha256:b8a9b1c357d2880af1a629c3980fdd0d74708bdedf0bce14c0aa4f6d90fddedd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24` - linux; amd64

```console
$ docker pull maven@sha256:d82406df6ca601db46426256e23912d4651171fc225fd417e9f9fabed22a445d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.2 MB (335152856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7b416383812f070e5f31a48d0bb3e37d836ceb259d8d550f357a1415f515d0c`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ARG version=24.0.1.9-1
# Thu, 27 Mar 2025 16:03:48 GMT
ARG package_version=1
# Thu, 27 Mar 2025 16:03:48 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 27 Mar 2025 16:03:48 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec66c391cf9a3d196d14d11e9af9cf5afbdc77df45f01f053c094f4c9c106d6`  
		Last Modified: Fri, 13 Jun 2025 17:12:58 GMT  
		Size: 187.2 MB (187192771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01c3d95a642ca3e77a87ea57e305797ed62f278b0244481eee1a814e1e3d3847`  
		Last Modified: Fri, 13 Jun 2025 17:23:40 GMT  
		Size: 85.2 MB (85218245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:040acf5f5a05a4da3480763566451ebebc045917bf8bcdfd55b41763060554ea`  
		Last Modified: Fri, 13 Jun 2025 17:23:25 GMT  
		Size: 9.2 MB (9170439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4123fac7648c2d386fd0228d1bed870d4d8c5c3c0f67d1226e298096eaa5e67c`  
		Last Modified: Fri, 13 Jun 2025 17:23:24 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad63eb9fcaccef8f5de113146694e93400b36c8e5145f5dfa5a54139f1768302`  
		Last Modified: Fri, 13 Jun 2025 17:23:24 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:163f25d20d3afc6a12008b1890675b2511be9d2f436f4dd3be06733c557d5b95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6220829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2967b7bdbce1861813ff094c0b9bf41f0c17b6b7f49bbb045fa5b77d827d85`

```dockerfile
```

-	Layers:
	-	`sha256:bba966b11325f89b5c6c278336b19233a6cad605c1af81315f794ae4eb08e0c4`  
		Last Modified: Fri, 13 Jun 2025 20:27:53 GMT  
		Size: 6.2 MB (6204523 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31c49ed3b3b5bc9b0e3b67df8dc0d6533d022188268f833b4290f8157f998b35`  
		Last Modified: Fri, 13 Jun 2025 20:27:54 GMT  
		Size: 16.3 KB (16306 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:cee13e35755a3682006dcc6c013ad9b535fd844e88e3f33dd3f242f99bdad1e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.3 MB (329345111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52db18dda447105ecddc7a14b56e8e4e0e3075cdfed4928e5e341b6f48177bba`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ARG version=24.0.1.9-1
# Thu, 27 Mar 2025 16:03:48 GMT
ARG package_version=1
# Thu, 27 Mar 2025 16:03:48 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 27 Mar 2025 16:03:48 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606c71bde4a7d05e0626f9b64fb3e0bc776c63157501c509a656a16ad481691`  
		Last Modified: Tue, 20 May 2025 07:19:50 GMT  
		Size: 185.2 MB (185232892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04b115917a0af052e577314c926f097353a3d78deabe8111ab955ceac5e12c48`  
		Last Modified: Tue, 03 Jun 2025 14:25:16 GMT  
		Size: 82.4 MB (82374997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90209d3a4ff1f65317c35a6591b0004fe472df0bc12d41119a71b459319df843`  
		Last Modified: Tue, 03 Jun 2025 14:25:10 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff51256513abe671a1acb7621723597fbfa69487612c13e2a447f4bcd44d9591`  
		Last Modified: Tue, 03 Jun 2025 14:25:09 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c32a67678ae5bd91abd0b4ce775f1ba72691ffe9d855e862b1172d0d6404d14b`  
		Last Modified: Tue, 03 Jun 2025 14:25:09 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:3b1fe8d64a9a274b33349793578b410e81d7ea57289d98aca3cffdbd3b7cd174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6216891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45f498960db8ba5656f97cc2d963507eb78c196e13e9249d1daf1b9c8459f44b`

```dockerfile
```

-	Layers:
	-	`sha256:d7fb94416476185cf04ef70665d97672e0478216ad6487cac3376e03ef234d56`  
		Last Modified: Tue, 03 Jun 2025 17:28:35 GMT  
		Size: 6.2 MB (6200453 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61e37454a4b1e38d51dedbf35157b2752ffa000beccb4dd53204979963c4a28c`  
		Last Modified: Tue, 03 Jun 2025 17:28:36 GMT  
		Size: 16.4 KB (16438 bytes)  
		MIME: application/vnd.in-toto+json
