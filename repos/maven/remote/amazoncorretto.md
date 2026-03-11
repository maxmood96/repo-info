## `maven:amazoncorretto`

```console
$ docker pull maven@sha256:d06313f1d44c4c836881f1470b225af620b2e1219f9b38b3a6fa057cb25e8145
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:792a57346f7c8ddb0e91ab81c908e7510560d2c69f6faf9b61be23b5fef8424c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.3 MB (368253982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4768939225878bc4eaa44ec8d341ef781d55e9b30f55a5149a592e50ca5ab926`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:25 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:25 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:25 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:16:52 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 11 Mar 2026 19:16:52 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:16:52 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:52 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:16:52 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:16:52 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:16:52 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:16:52 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:16:52 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:16:52 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:16:52 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:16:52 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:16:52 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:16:52 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:16:52 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1899f99dbf61d2e92bf9bc374b2f4ec7c5b8a1687b8543b4ecc212164833f14`  
		Last Modified: Wed, 11 Mar 2026 18:34:50 GMT  
		Size: 189.2 MB (189186371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f62e6a066e5598402535f63481abd6128936f7e153ac1cafc92896e8c7814c1`  
		Last Modified: Wed, 11 Mar 2026 19:17:12 GMT  
		Size: 115.3 MB (115335951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4df3fcdbd675e8ded4e1b7b5d576448723686cda296883bceb61bb06b90155`  
		Last Modified: Wed, 11 Mar 2026 19:17:08 GMT  
		Size: 9.7 MB (9697526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9335ebe064b3021e9ece8d6b6f7cc49086e2667e52034c629fe943c884b22628`  
		Last Modified: Wed, 11 Mar 2026 19:17:08 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89202dc2c80ed9d932ea8fab06528a73ef36482fd4ad8c86d2efa066fc39d7c2`  
		Last Modified: Wed, 11 Mar 2026 19:17:08 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:33732337bd5677f7e6d869e7ae4878f0dcae0cbca27711b1e93d586ccd8ecd69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6233123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db6e8242d2a65b808703c2eeb3b54e35f47bca086288091db0983332ec56d450`

```dockerfile
```

-	Layers:
	-	`sha256:62c3c74bdcb085875a58afeb96774bf9b3e6ada7f8e348fa382ad9bc61159bea`  
		Last Modified: Wed, 11 Mar 2026 19:17:09 GMT  
		Size: 6.2 MB (6215574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9561aa80f26a140d4930337f3fef79eaee40cf1b215ebf465ab8d9934fbea0d8`  
		Last Modified: Wed, 11 Mar 2026 19:17:08 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:006d226b53ef6e046cfb3055419ef3bb4230005af9f50bb4baf70dddff933874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.1 MB (364077431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87dd3492c978b72b2a9e08bcc488f6b0ce2ec7d172c7c114112cb9616ff7f1e1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:05 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:05 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:05 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:05 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 11 Mar 2026 19:17:05 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 11 Mar 2026 19:17:05 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 11 Mar 2026 19:17:05 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:05 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 11 Mar 2026 19:17:05 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 11 Mar 2026 19:17:05 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 11 Mar 2026 19:17:05 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 11 Mar 2026 19:17:05 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 11 Mar 2026 19:17:05 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 11 Mar 2026 19:17:05 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 11 Mar 2026 19:17:05 GMT
ARG MAVEN_VERSION=3.9.13
# Wed, 11 Mar 2026 19:17:05 GMT
ARG USER_HOME_DIR=/root
# Wed, 11 Mar 2026 19:17:05 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 11 Mar 2026 19:17:05 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 11 Mar 2026 19:17:05 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9ab420359a2ce38b24b838a3ea4b4bcbfe85a0c06909eead4a8cca721947cb`  
		Last Modified: Wed, 11 Mar 2026 18:34:30 GMT  
		Size: 187.1 MB (187088807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd94fd2673d0c4688fcca5c621cf2d624f7da1c8f30450a23726762bbd75940`  
		Last Modified: Wed, 11 Mar 2026 19:17:23 GMT  
		Size: 114.3 MB (114348653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e3fa5d4cbae643a62ed36d9511d98e2f1c98970ca97e9286ca6900fda034ce`  
		Last Modified: Wed, 11 Mar 2026 19:17:21 GMT  
		Size: 9.7 MB (9697555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0dd0d8523c12f87e3ebfa046348511bc163ee2a210d502685b6750878b1a2b7`  
		Last Modified: Wed, 11 Mar 2026 19:17:20 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f3c24924e342f35c417fbacf5d3e092aab18d7f54f732c24216823a8633c2fc`  
		Last Modified: Wed, 11 Mar 2026 19:17:21 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:65ae69cc6a17129a2df13a6cbf9c30369b4c2add0baad04a7ffb8b72c585e0ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6232296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432a453ae17376ee9963539f3d765b2c2f7316deccfa7df26899c4891cc7d19b`

```dockerfile
```

-	Layers:
	-	`sha256:878d4da31661790cf91c8d31ccaa463f832c73341b957ceb90eb3b0478fb19ea`  
		Last Modified: Wed, 11 Mar 2026 19:17:21 GMT  
		Size: 6.2 MB (6214566 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2762c1fc143773d2ec2f4f694440fdff366578cc1660b6ca23ac3fff1be12ae1`  
		Last Modified: Wed, 11 Mar 2026 19:17:20 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
