## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:65e06d061800aa5c3c27df0c589c5ba9386bfe0cee7821ec4b2208285217fb73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:95ff33d635a396c272bb8ce27562e47bbd75ff3a272b27f7272e44190fd6b38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **372.4 MB (372385354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86f12d274d1cde85a6e500a04ae696772a390578f3f016f07f91c05af1cfd50e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:34 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:34 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:05:12 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:05:12 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:05:12 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:05:12 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:05:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:18:34 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 22 Jun 2026 18:18:36 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 22 Jun 2026 18:18:36 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 18:18:36 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:18:36 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:18:36 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 18:18:36 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 18:18:36 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 18:18:36 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 18:18:36 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 18:18:36 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 18:18:36 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 18:18:36 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 18:18:36 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43a4ccfcda545d0357b8595db01c68db022db4283c68d08e06427e6c91ac7063`  
		Last Modified: Sat, 13 Jun 2026 02:07:52 GMT  
		Size: 54.6 MB (54574183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebbda8bbed2402313490b832b371f9a31cefa72cc0c1f79f7de0207d319faaf9`  
		Last Modified: Mon, 22 Jun 2026 18:05:38 GMT  
		Size: 170.4 MB (170446421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eba4d34de6a5353260a49adb66fd14c5d2b9c0f25537980074cbcb2428bf6a3a`  
		Last Modified: Mon, 22 Jun 2026 18:18:54 GMT  
		Size: 125.5 MB (125472718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68f12294afa58fc0a65f97bd901bbe6ded7b0a3283abb013af502cbfa568405`  
		Last Modified: Mon, 22 Jun 2026 18:18:51 GMT  
		Size: 12.5 MB (12531047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6681368f972108c9017dae5f19692243ae4bcc2a20448c13527589c5bf2aa9d6`  
		Last Modified: Mon, 22 Jun 2026 18:18:52 GMT  
		Size: 9.4 MB (9359974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f88a7bfd902d8d0891fe23878d334f52b59ec28964f69c1e8b5119413064331a`  
		Last Modified: Mon, 22 Jun 2026 18:18:51 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b5d659818c0ef3387d0dea667a8decde4d6d721f8aa4c40de1242ead3c0b290`  
		Last Modified: Mon, 22 Jun 2026 18:18:52 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d70989ef3ac54ae9a0d4ea06bfb73cd8dc4aa2dcd8986e64211e7b37d0112927
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6263761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e82e37d49da063c8e04a02d2aa59aea10d1944f0a4386837100144e0cf2daf3f`

```dockerfile
```

-	Layers:
	-	`sha256:0d8262e86428da153c1436fa65037bf67c4604367b4a5463cc667d7175106f90`  
		Last Modified: Mon, 22 Jun 2026 18:18:51 GMT  
		Size: 6.2 MB (6247473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d893bf40d06a241db0f3bcf6f88cc71fd2d15dd079165b6e1740673c88e3251`  
		Last Modified: Mon, 22 Jun 2026 18:18:51 GMT  
		Size: 16.3 KB (16288 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:4fd16ac938ab399b88e94c8d82f6d18481d50e7eaa725e2010b44d163099b20b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368294525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1475571bfc9ea90ee374055876e00188bf0f121d3d7926e674abab89705fbec`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 22 Jun 2026 17:59:55 GMT
COPY /rootfs/ / # buildkit
# Mon, 22 Jun 2026 17:59:55 GMT
CMD ["/bin/bash"]
# Mon, 22 Jun 2026 18:15:10 GMT
ARG version=21.0.11.10-1
# Mon, 22 Jun 2026 18:15:10 GMT
ARG package_version=1
# Mon, 22 Jun 2026 18:15:10 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 22 Jun 2026 18:15:10 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 18:15:10 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Mon, 22 Jun 2026 18:34:36 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 22 Jun 2026 18:34:38 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 22 Jun 2026 18:34:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 22 Jun 2026 18:34:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:34:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 22 Jun 2026 18:34:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 22 Jun 2026 18:34:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 22 Jun 2026 18:34:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 22 Jun 2026 18:34:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 22 Jun 2026 18:34:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 22 Jun 2026 18:34:38 GMT
ARG USER_HOME_DIR=/root
# Mon, 22 Jun 2026 18:34:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 22 Jun 2026 18:34:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 22 Jun 2026 18:34:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:9d73cc96eee98f0257861d2c8c5e7eac1d4fd5e92dd1ed16608b0040908eb5e0`  
		Last Modified: Fri, 12 Jun 2026 22:22:20 GMT  
		Size: 53.5 MB (53450686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10beb5c68f4d3c7d1c45314bbff9c0bb6baf58079563b749b2f64ac9f3c511d3`  
		Last Modified: Mon, 22 Jun 2026 18:15:34 GMT  
		Size: 168.7 MB (168721711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ce92d416421ac378a2c4ad601b46a579b5e0919e0287f611544baa0421a1d9`  
		Last Modified: Mon, 22 Jun 2026 18:34:59 GMT  
		Size: 124.0 MB (123973467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86e9f249956dfd71f67befa49ef3c277fd75c1d8b734f4e0ef248410c3f4e35`  
		Last Modified: Mon, 22 Jun 2026 18:34:56 GMT  
		Size: 12.8 MB (12787684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e010d2c949ef91152b9fe851a9a488a7ac9fef2d2ad565b838a461b63f3a0cbe`  
		Last Modified: Mon, 22 Jun 2026 18:34:56 GMT  
		Size: 9.4 MB (9359969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12dae99b91212a427bc332089e3baf508e24d48b74ee1decfc31846b91eea6eb`  
		Last Modified: Mon, 22 Jun 2026 18:34:55 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270b3f1865fd772e17d3917c87ae66ab715d960439b21f6d40c83379f550ea7f`  
		Last Modified: Mon, 22 Jun 2026 18:34:57 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:df6c5a28e67a0b1880e225663141d1c3f16651d9f700f626f491d22a87ea9902
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6262844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7db7e7cf20ebdbe0edcc77e87c3c0fa3606462d9ca022fe75e6dbd9f4b602c7`

```dockerfile
```

-	Layers:
	-	`sha256:6a9ce11d8d40c28e73b7bb51fa0ad5219c677121be292bfcd24a6f0aca10b001`  
		Last Modified: Mon, 22 Jun 2026 18:34:56 GMT  
		Size: 6.2 MB (6246407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bccd10b3765edc341c8ede9b821fe4d44eed631bdae770e2b08c1eee73eb5d3`  
		Last Modified: Mon, 22 Jun 2026 18:34:55 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
