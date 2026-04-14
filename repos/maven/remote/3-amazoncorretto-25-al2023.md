## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:6a3a981dd9a624843c596aedf67159eac5c09d9d7887b69036af7491d806a8f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5e11f7ebff41bb345c618f7ba70bbb3247a63242ad06092603334bdc05499ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **371.9 MB (371927631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda7f48fcfe56e75fbd2379dc317fc845a728769a921f54c495793042ab384f8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:49:36 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 22:49:36 GMT
ARG package_version=1
# Mon, 13 Apr 2026 22:49:36 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:49:36 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:49:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 13 Apr 2026 23:43:39 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 13 Apr 2026 23:43:39 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:43:39 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:43:39 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:43:39 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:43:39 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:43:39 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:43:39 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:43:39 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:43:39 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:43:39 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:43:39 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:43:39 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:43:39 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:43:39 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8965f1a19918fd21b127f9ac8bada2cedd82d65adae53850afab82d4eff565fd`  
		Last Modified: Mon, 13 Apr 2026 22:49:58 GMT  
		Size: 189.2 MB (189188193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:188e22a4118155811eda194cd0677c72ae51de21b4ae57b4d78471c62688df6b`  
		Last Modified: Mon, 13 Apr 2026 23:44:15 GMT  
		Size: 118.9 MB (118855964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ad1ca4236072ae904ae89003bc4ec38b89946818ff932754f342cd851eef34`  
		Last Modified: Mon, 13 Apr 2026 23:44:08 GMT  
		Size: 9.3 MB (9311179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928bb7c080c44e2bd4b629ad2b2565382f24d6da97a3197e1ad613d120675049`  
		Last Modified: Mon, 13 Apr 2026 23:44:01 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd481848b3cccefd11802d20a9da399344b94411019145973b7cb7d0935a495`  
		Last Modified: Mon, 13 Apr 2026 23:44:02 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:52dc605dfbf5e995f7c424f43588daa1a7e327cf5b5a0a132678a0b7c73d68fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6230577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c85bf5c02fc88b382c035745696b26bc6d145ff8911577ea5043855bfb0bffa`

```dockerfile
```

-	Layers:
	-	`sha256:0d7d1ddf1466a6523ba577139af1a98b729504804285f6e5f5f591eb7576302a`  
		Last Modified: Mon, 13 Apr 2026 23:44:08 GMT  
		Size: 6.2 MB (6214227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c28d3827dae1a2550a205997c5d7eba7090a17e4019a3a96b441833bb60b2c1d`  
		Last Modified: Mon, 13 Apr 2026 23:44:00 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8f027552d4aab5fd5a325f412dc1efea0928fe9877482f790d7ba7d6b9bc4f86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.8 MB (367835929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3eb35cfd45568ddf18315b3118c124625e9a7f875cc0792f9ad481105a56accb`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:12:21 GMT
ARG version=25.0.2.10-1
# Mon, 13 Apr 2026 23:12:21 GMT
ARG package_version=1
# Mon, 13 Apr 2026 23:12:21 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:12:21 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:12:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Mon, 13 Apr 2026 23:56:57 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 13 Apr 2026 23:56:57 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:56:57 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:56:57 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:56:57 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:56:57 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:56:57 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:56:57 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:56:57 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:56:57 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:56:57 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:56:57 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:56:57 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:56:57 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:56:57 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4012a6eeb902fd47c054143eafd4fb0b52ee79fd3d3e5359b5394be8cad6db3`  
		Last Modified: Mon, 13 Apr 2026 23:12:47 GMT  
		Size: 187.1 MB (187089592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10a415754380acc6cabf2f11dc271722952f3b451e5ccddffc38512ac5dc5f9`  
		Last Modified: Mon, 13 Apr 2026 23:57:16 GMT  
		Size: 118.0 MB (117991382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b479b6a59a741823a1f9c37f0442060676f6db24e1afc693124ac138e1a8e425`  
		Last Modified: Mon, 13 Apr 2026 23:57:13 GMT  
		Size: 9.3 MB (9311175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb3dac821df396988208e7841c55c3307c9a17b57e8caaab30cae6dfb9038c9`  
		Last Modified: Mon, 13 Apr 2026 23:57:13 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:024b79644152cdb8e90e714396a767712b0a5ec5e9c34773267932ee707276e9`  
		Last Modified: Mon, 13 Apr 2026 23:57:13 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:59aa19a366914a215f5163bacc1f300ab893b22468e47cc351f1c87f29808d6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6229654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca172804e9dcb1d90b2032fc2fd8c43174188f86dcfad76e2527ce17ad0efa3f`

```dockerfile
```

-	Layers:
	-	`sha256:72efc05a93ea62bfedd4b684972ce41728a5b2081e1dc21bf381c7cf6e5618df`  
		Last Modified: Mon, 13 Apr 2026 23:57:13 GMT  
		Size: 6.2 MB (6213171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c910faeba18b5f19b3c8af3654c755d54fa11e07e2f842c7e493f5ab9d7aabfc`  
		Last Modified: Mon, 13 Apr 2026 23:57:13 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
