## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:1111b4cadce9be9d350bfb4bb41d619e3a8a69cced05c9a65517d86dff699dd8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:7df0e757963072fa7bfd751a1c53f4099dc2a0b1b6467ffc6cfd7670d547cd99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.6 MB (338550410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f569c905c4c0785c6bbef2a16047983e7b23c3968f984582d4fbf574181cd100`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:40 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:40 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:40 GMT
# ARGS: version=21.0.9.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:40 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:15:28 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 31 Oct 2025 01:15:30 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:15:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:15:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:15:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:15:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:15:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:15:30 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:15:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:15:30 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:15:30 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:15:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:15:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:15:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74b4a5d42de3c0bca4195fdbee7ccdbbaad50ab5ac755ccf13f0bd242283a472`  
		Last Modified: Fri, 31 Oct 2025 01:11:10 GMT  
		Size: 170.2 MB (170207572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ce421cb72b3096cf3e7babd2a8348b504187e9aee492177c608639fef85efe`  
		Last Modified: Fri, 31 Oct 2025 01:16:12 GMT  
		Size: 92.6 MB (92577622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f0edf1aa69a7b6f439bcf137b1b7b1a6b40543d31fdb9cc8c9f6a2af398f21`  
		Last Modified: Fri, 31 Oct 2025 01:15:53 GMT  
		Size: 12.5 MB (12520354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aad8e9ef4c1573965d3062b8ca23bead6a48cfb1216078bc254b28365ebecd4`  
		Last Modified: Fri, 31 Oct 2025 01:15:52 GMT  
		Size: 9.2 MB (9242587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72aede7347d8094c5c3897f69cd22ced62cf7dffa78ea9b273541730642b5e88`  
		Last Modified: Fri, 31 Oct 2025 01:15:51 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2587890790d1407372acd015255c7e1a09aab3651610c37fbc0d59034a0a973`  
		Last Modified: Fri, 31 Oct 2025 01:15:52 GMT  
		Size: 156.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:466236b874802f3a0a8dc59c67ba779be0a982c99294e45e90ce7bc3a969b1a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6252723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef462da2d08285bb17b72090292718bb6ef2d4d63f5ae7b202c3b4ddc90bd71`

```dockerfile
```

-	Layers:
	-	`sha256:6edb6b57667c1746f567af739d8ed942c6cc4a999e08cf0d9f948216f382ca51`  
		Last Modified: Fri, 31 Oct 2025 02:28:19 GMT  
		Size: 6.2 MB (6234438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4186f592f03002fec7030cbd315bbf83f554722b81547519c2a1ef3520fd4d6b`  
		Last Modified: Fri, 31 Oct 2025 02:28:19 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f061dd73b72b78c5960eb226bf53ee9d3be8ed480174352a6f66bd2be9973642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **335.0 MB (335023585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdd83ce8b378b5282787dd66d7a86159db0c64f89df85696bfd8bbb2985c61e1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:57 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:57 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:57 GMT
# ARGS: version=21.0.9.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:57 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
# Fri, 31 Oct 2025 01:15:23 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 31 Oct 2025 01:15:26 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 31 Oct 2025 01:15:26 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 31 Oct 2025 01:15:26 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:26 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 31 Oct 2025 01:15:26 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 31 Oct 2025 01:15:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 31 Oct 2025 01:15:26 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 31 Oct 2025 01:15:26 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 31 Oct 2025 01:15:26 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 31 Oct 2025 01:15:26 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 31 Oct 2025 01:15:26 GMT
ARG MAVEN_VERSION=3.9.11
# Fri, 31 Oct 2025 01:15:26 GMT
ARG USER_HOME_DIR=/root
# Fri, 31 Oct 2025 01:15:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 31 Oct 2025 01:15:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 31 Oct 2025 01:15:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed77e24e263615113568f971380ee95108409043a4dc2ccda5b462e834b7a960`  
		Last Modified: Fri, 31 Oct 2025 01:11:28 GMT  
		Size: 168.5 MB (168475202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35600b507597b8f2e7f5412bd159f11376818526bb86fb7d433f902823eb0a4e`  
		Last Modified: Fri, 31 Oct 2025 01:16:04 GMT  
		Size: 91.6 MB (91625533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88474fbb727f5748a095e6b431a5ad5f4c225a27bfbf4392008e7961ea5a480d`  
		Last Modified: Fri, 31 Oct 2025 01:15:51 GMT  
		Size: 12.8 MB (12777373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80076bc42b71ac24236452900f4f209bec60ff80cf0f3f3cdf5806f05de98214`  
		Last Modified: Fri, 31 Oct 2025 01:15:51 GMT  
		Size: 9.2 MB (9242584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72d1f56d8c65d51b742ecbcc3fecc7db4439492b81c767a571f1b493626ad2a`  
		Last Modified: Fri, 31 Oct 2025 01:15:50 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef7478a535e1372de58576ed43852751fcab2329d8509ad6663355ee1de03664`  
		Last Modified: Fri, 31 Oct 2025 01:15:50 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:b957cbd35851251b2cace1017136c3a93b032ebd18fd10ccc923064ad843b339
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6251804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a63faed4875ec87ce70d7de488f907d3f79a769b839daee21847c5a4cde23fd9`

```dockerfile
```

-	Layers:
	-	`sha256:2251961c39bbe163aafb05963e4cf018c379a7264665826cbabfefc2230088e5`  
		Last Modified: Fri, 31 Oct 2025 02:28:25 GMT  
		Size: 6.2 MB (6233371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cdc4583c061172b07b77883dd31ec88f246cd173c9338e0140a83581df666ad`  
		Last Modified: Fri, 31 Oct 2025 02:28:25 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
