## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:a2aef377e572b6868ade54e77c0e47c039490320490eeabeec66b62702793e66
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:3bf101d10f466516f02ffc3ceb34aa82b6b049a4d8c3617d6ad89a47f72d346b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.9 MB (331858995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3955fc64385d2ecb4968762c43ed354a8110111ce63fe9818f343c454dc2d1fe`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 15 Jan 2026 21:43:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:43:45 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:08:44 GMT
ARG version=17.0.17.10-1
# Thu, 15 Jan 2026 22:08:44 GMT
ARG package_version=1
# Thu, 15 Jan 2026 22:08:44 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 15 Jan 2026 22:08:44 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:08:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Fri, 16 Jan 2026 02:44:15 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Fri, 16 Jan 2026 02:44:18 GMT
RUN yum install -y openssh-clients # buildkit
# Fri, 16 Jan 2026 02:44:18 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 16 Jan 2026 02:44:18 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:18 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 16 Jan 2026 02:44:18 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 16 Jan 2026 02:44:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 16 Jan 2026 02:44:18 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 16 Jan 2026 02:44:18 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 16 Jan 2026 02:44:18 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Fri, 16 Jan 2026 02:44:18 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 16 Jan 2026 02:44:18 GMT
ARG MAVEN_VERSION=3.9.12
# Fri, 16 Jan 2026 02:44:18 GMT
ARG USER_HOME_DIR=/root
# Fri, 16 Jan 2026 02:44:18 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 16 Jan 2026 02:44:18 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 16 Jan 2026 02:44:18 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:ed23be565800a5983cd3d8b6fd581e584110f08d9e32684d0eb5ab2820cadcbc`  
		Last Modified: Wed, 07 Jan 2026 22:09:37 GMT  
		Size: 54.0 MB (54021204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fc6640824248aca505f62c333fc0318225d8793a5947ba1d4471ee182eb329`  
		Last Modified: Thu, 15 Jan 2026 22:11:52 GMT  
		Size: 156.9 MB (156901421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179946dd237895ea37d18ca988f7806943caec9fa828f020f0627ea4095b4c35`  
		Last Modified: Fri, 16 Jan 2026 02:45:05 GMT  
		Size: 99.1 MB (99126429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cafdccc005d69ac83f66650b2fabc1a95933d86fd277bc6b5637bf63d53ff03`  
		Last Modified: Fri, 16 Jan 2026 02:44:42 GMT  
		Size: 12.5 MB (12496658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ff0028963e95e5ba044391da8ab0236db8936be2eece51fa4ccf6d04d62c1ce`  
		Last Modified: Fri, 16 Jan 2026 02:44:42 GMT  
		Size: 9.3 MB (9312244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:871a4ee5ec9fdd59473ace7a7ffc4f4ddee561ac1ab8d47621327d47b8acb531`  
		Last Modified: Fri, 16 Jan 2026 02:44:41 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eafa1d7e02bbb04898d9ef2d06f0f37457f2af7fbf0f675c30e0996f66f28d0`  
		Last Modified: Fri, 16 Jan 2026 02:44:41 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:b7df6f137a0bd56bf415f6c02326fcfb6928d650825049076ba93ccc78d9ceb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6250320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a36ade11a98d350fd6d99f2c9e9b428cd63a5cb7f68d3eb879f44748c07754b`

```dockerfile
```

-	Layers:
	-	`sha256:9e74061ac9680987ab9806c5e31cd73119433bbbf996c7d7ee1ebc68ea1b9a1a`  
		Last Modified: Fri, 16 Jan 2026 03:28:54 GMT  
		Size: 6.2 MB (6232035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c5a2aec28e09cba73fcaaaddff5aefd4f8ec66458204124625300801a0ffc80`  
		Last Modified: Fri, 16 Jan 2026 03:28:55 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:73855c2881b9c9639d6f8c1a3d475c43337bfd718a37bf819a5ada1c124a6548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.6 MB (325635233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:305390334bb2cd36595bd8bd7e2533c173028dcf9861e259c1fbc661310409c9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:29 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:29 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:26:29 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:26:29 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 18 Dec 2025 02:22:55 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 18 Dec 2025 02:22:58 GMT
RUN yum install -y openssh-clients # buildkit
# Thu, 18 Dec 2025 02:22:58 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 18 Dec 2025 02:22:58 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:22:58 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 18 Dec 2025 02:22:58 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 18 Dec 2025 02:22:58 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 18 Dec 2025 02:22:58 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 18 Dec 2025 02:22:58 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 18 Dec 2025 02:22:58 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 18 Dec 2025 02:22:58 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 18 Dec 2025 02:22:58 GMT
ARG MAVEN_VERSION=3.9.12
# Thu, 18 Dec 2025 02:22:58 GMT
ARG USER_HOME_DIR=/root
# Thu, 18 Dec 2025 02:22:58 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 18 Dec 2025 02:22:58 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 18 Dec 2025 02:22:58 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:222f9dca445f419513819266ddecf7477b069aa5b3d4e331702639766d5ce2a1`  
		Last Modified: Thu, 18 Dec 2025 01:27:19 GMT  
		Size: 155.7 MB (155707401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2951d3bff5c5324cffa4c69754de59ede67139ceb5d04c022a0f33147bae76f1`  
		Last Modified: Thu, 18 Dec 2025 02:23:38 GMT  
		Size: 95.0 MB (94991089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60e85800bfde2f1897296b87898ee4decd71bc2f0230acec1c1d206b44f023bd`  
		Last Modified: Thu, 18 Dec 2025 02:23:22 GMT  
		Size: 12.8 MB (12750005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d72413bf8d66e01092f69450a5211e219b79bb97364c143c11eb5be5c320d4c`  
		Last Modified: Thu, 18 Dec 2025 02:23:22 GMT  
		Size: 9.3 MB (9312248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e1413fedca0f2c16a4de27e5c27654f65fb76502607cbccf2281a9e344d476`  
		Last Modified: Thu, 18 Dec 2025 02:23:22 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4e235a0cca54947a9bae00c18d12d845f92639d8dc0c91e675293d8dfdeb8b`  
		Last Modified: Thu, 18 Dec 2025 02:23:21 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:6f8f15d6ed6183bc494495efe81214b142d70e9e2e141851218803f3aa4e394a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6249394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29e12d558c618b298a8fdcb0efea807440fea7cf96dff2189ffbf3abbc7e6f13`

```dockerfile
```

-	Layers:
	-	`sha256:1048ee0e12e0bf92fb801dfe1940c9287e25bd1bff19fe2344d039d97acc3af6`  
		Last Modified: Thu, 18 Dec 2025 03:28:10 GMT  
		Size: 6.2 MB (6230961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e654cb38695fead8cebb401fd48eda77f9ef4541093b0945c8cc19840fbe64f`  
		Last Modified: Thu, 18 Dec 2025 03:28:11 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
