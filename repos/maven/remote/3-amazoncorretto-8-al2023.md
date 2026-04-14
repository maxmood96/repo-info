## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:775faa8c109226c1147703736d6fb7f29eb59172362e5ab1b5e42496b61f8b60
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:59c84cd7af4a9f886928d1aec298f0da87d51c16199bbb549b644e3117901be7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.7 MB (511662015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a8d55b6fdbc437b909937529e3a4a4cad84869ebc4fa778e42975c210bba20`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:05 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 22:48:05 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:48:05 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 13 Apr 2026 23:44:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 13 Apr 2026 23:44:08 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:44:08 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:44:08 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:44:08 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:44:08 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:44:08 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:44:08 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:44:08 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:44:08 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:44:08 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:44:08 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:44:08 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:44:08 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:44:08 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:44:08 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b1983f26d4f73d2638487eb5a60254859b1629d25024622b419593661d40b82`  
		Last Modified: Mon, 13 Apr 2026 22:48:58 GMT  
		Size: 330.9 MB (330921442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb319bb1fa066f59715062d67f757810e5c11157d97ca0a5f2c31960b04f1bc7`  
		Last Modified: Mon, 13 Apr 2026 23:44:39 GMT  
		Size: 111.4 MB (111401133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917fa3857a708c20a9cd8852aa2587d1547ce2ae09f43c7c3af9ffdbff418af1`  
		Last Modified: Mon, 13 Apr 2026 23:44:36 GMT  
		Size: 5.5 MB (5455953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1561d54ffedf2d3abbb870030b168d3d920fab35f16c93b8d05f7482c35b74e8`  
		Last Modified: Mon, 13 Apr 2026 23:44:36 GMT  
		Size: 9.3 MB (9311191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4a48aa901c3a621fd4db546b2b4de2c9e98f1f0cb0ce1469de483df5baf55a8`  
		Last Modified: Mon, 13 Apr 2026 23:44:36 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ade9e1770d328bb73b65dee9b3fe4756fb43a6f627ba0d50f1d58fe58fe4c31`  
		Last Modified: Mon, 13 Apr 2026 23:44:37 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:5f362827446403c30c290fb95397855e84ecbc5eb0fa54ae93948a717ad8eab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.9 MB (13852933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80d6f811cd6dd3fafdef7fb51374312a7a406942a33fc9401a8899c0735f858`

```dockerfile
```

-	Layers:
	-	`sha256:16b36b7f568c9dca223b8d243d011bde68f19f48b20331e6ef6d8ed680bc74ce`  
		Last Modified: Mon, 13 Apr 2026 23:44:36 GMT  
		Size: 13.8 MB (13834652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8f06ce770cc14125e547bfecc4a12b139c8570c718fb14878f8bac3e4187df7`  
		Last Modified: Mon, 13 Apr 2026 23:44:36 GMT  
		Size: 18.3 KB (18281 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b2808abc21c59d8adab6ad88cb3986471bc133753b99f1f98736a45ccd7771b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **301.4 MB (301387691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7687be2e49df1ac83fa562f73abb3656b6809930f30408b45ed8fda454a1c7`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:10:29 GMT
ARG version=1.8.0_482.b08-1
# Mon, 13 Apr 2026 23:10:29 GMT
# ARGS: version=1.8.0_482.b08-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.${ARCH}.rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:10:29 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:10:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
# Mon, 13 Apr 2026 23:57:24 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Mon, 13 Apr 2026 23:57:27 GMT
RUN yum install -y openssh-clients # buildkit
# Mon, 13 Apr 2026 23:57:27 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 13 Apr 2026 23:57:27 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:57:27 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 13 Apr 2026 23:57:27 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 13 Apr 2026 23:57:27 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 13 Apr 2026 23:57:27 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 13 Apr 2026 23:57:27 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 13 Apr 2026 23:57:27 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 13 Apr 2026 23:57:27 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 13 Apr 2026 23:57:27 GMT
ARG MAVEN_VERSION=3.9.14
# Mon, 13 Apr 2026 23:57:27 GMT
ARG USER_HOME_DIR=/root
# Mon, 13 Apr 2026 23:57:27 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 13 Apr 2026 23:57:27 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 13 Apr 2026 23:57:27 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cd51fd7ccca75a0b426896e7519c1bd14d9d834f603f074a9f60c9b5d277a41`  
		Last Modified: Mon, 13 Apr 2026 23:10:49 GMT  
		Size: 118.0 MB (117962706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ee6243d0b46879c1f1e85e02b28d41d2cfbcf158fecd6c712d5f39214746b54`  
		Last Modified: Mon, 13 Apr 2026 23:57:46 GMT  
		Size: 107.9 MB (107895709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f0225e26de1a7a121f94da28b30f3d62e225c3d03752b9ebb8b66ea92f5c075`  
		Last Modified: Mon, 13 Apr 2026 23:57:44 GMT  
		Size: 12.8 MB (12774320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:758baa30b1456efb7e4eec43f112e00c40ce705f8d9f24d7f43bde15bfb57570`  
		Last Modified: Mon, 13 Apr 2026 23:57:44 GMT  
		Size: 9.3 MB (9311175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c141761e8abff73f6438871fabbb81f82629a36ec7f29c112a3cf492f378aa1`  
		Last Modified: Mon, 13 Apr 2026 23:57:43 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f089e04a836dbc49c9b6c6c9ec9aa55738c717eedde543a218ab8e2cb613bf1a`  
		Last Modified: Mon, 13 Apr 2026 23:57:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:ab9b8171a0d9b011f73528e40262def74d3eb205dcbf0845e5e1a4267593e527
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6634408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83ce53c20ac8b80b29a83dc8067602e385ed1bfd0715fc9ce6629bec3df4c23d`

```dockerfile
```

-	Layers:
	-	`sha256:8c6f57a487c705bf6cecd65681f4817349b00f758be6904c8bbb26264cf35205`  
		Last Modified: Mon, 13 Apr 2026 23:57:44 GMT  
		Size: 6.6 MB (6615973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb5c82e300b09b42c8f1ecd789591e9fcab389c20179fd893ec0f2a519d2a580`  
		Last Modified: Mon, 13 Apr 2026 23:57:43 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json
