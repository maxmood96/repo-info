## `maven:3-amazoncorretto-23-al2023`

```console
$ docker pull maven@sha256:2667dcd97ea585b473829f66347ea0960688b1c391b9264149f6c473ddf05de7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-23-al2023` - linux; amd64

```console
$ docker pull maven@sha256:2f37bc6b3d897643746c22297c7dfe0bbc26030f6f672edb859edb609559ba2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **309.8 MB (309771818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7265e980f67feefe23760474432601059e1619b14395305d5cd6725dd197be62`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.2.7-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68110f55e6e36ee4a99f72f6e365abe89668974e38522697508bf1386144fa59`  
		Last Modified: Thu, 23 Jan 2025 18:27:43 GMT  
		Size: 177.6 MB (177575238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81d1243ef458f396c81f7e95572b4de31fb2fcc786b55a3bf3c19539a0d62bf`  
		Last Modified: Thu, 23 Jan 2025 19:27:22 GMT  
		Size: 69.9 MB (69874626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e833c2446eef7e583c6840828b4d7eee17545ee17fde7b866e1bcc6c37420e`  
		Last Modified: Thu, 23 Jan 2025 19:27:19 GMT  
		Size: 9.2 MB (9170434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a1106535b383405c776721a5929fd310e7f48bed3a09c1b16bc7b4a5bde5ac`  
		Last Modified: Thu, 23 Jan 2025 19:27:19 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aef3ef67a865d534956ddb4ba31e84a889ecdf45742076b2850e69bf0d89da9`  
		Last Modified: Thu, 23 Jan 2025 19:27:22 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:2128afe2465302d9132a2727006848547b65fb045f616b7d974f1fa4620669bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6206524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e367179c41ac63ce991b8f3cc01283f2887a6699084fa921487d775c7d3e092`

```dockerfile
```

-	Layers:
	-	`sha256:08bbd03c83a13d362458951c262db0aa8948a8a52180fa386bf31976e9e0273e`  
		Last Modified: Thu, 23 Jan 2025 19:27:19 GMT  
		Size: 6.2 MB (6190147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b75cdb738a3ef49291069869c9603b54399c051d0353177db0f8d34105370ad`  
		Last Modified: Thu, 23 Jan 2025 19:27:18 GMT  
		Size: 16.4 KB (16377 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-23-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:b8edc3d582ff226c9ec2af808edecfb94db936e8f2cbfec80ee7fde5cceddf45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.7 MB (306693596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7cda2278d5190ceeec7b64472b10936dee37fde47069334d60ec3bbc5ee62f1`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /rootfs/ / # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["/bin/bash"]
# Mon, 23 Sep 2024 19:11:46 GMT
ARG version=23.0.2.7-1
# Mon, 23 Sep 2024 19:11:46 GMT
ARG package_version=1
# Mon, 23 Sep 2024 19:11:46 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ENV LANG=C.UTF-8
# Mon, 23 Sep 2024 19:11:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
# Mon, 23 Sep 2024 19:11:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Mon, 23 Sep 2024 19:11:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Mon, 23 Sep 2024 19:11:46 GMT
ARG MAVEN_VERSION=3.9.9
# Mon, 23 Sep 2024 19:11:46 GMT
ARG USER_HOME_DIR=/root
# Mon, 23 Sep 2024 19:11:46 GMT
ENV MAVEN_CONFIG=/root/.m2
# Mon, 23 Sep 2024 19:11:46 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Mon, 23 Sep 2024 19:11:46 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8e38bffa7f410a51ec3bb0ecab65fc8634f2b5d92215a3cb03fc47eeeab80d2`  
		Last Modified: Thu, 23 Jan 2025 18:54:47 GMT  
		Size: 175.6 MB (175608960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d282d7894c443a7019a4a816dbca441f3fc921798bb6be0ce8223d55670bc2ef`  
		Last Modified: Thu, 23 Jan 2025 20:00:18 GMT  
		Size: 69.6 MB (69644963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b6cc5b38c463b461b4aa441b51cb37ad0df56c98a7040c38b9a5e105104d2de`  
		Last Modified: Thu, 23 Jan 2025 20:00:17 GMT  
		Size: 9.2 MB (9170433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80f7d98f961c1b2bb0d7dca24a2a98900ad97e06111b5f87debd6744acb34f9d`  
		Last Modified: Thu, 23 Jan 2025 20:00:18 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac9590e7b283586aeda82e0bc79a8d3adf0131d235c2663b3636489b88e58a2`  
		Last Modified: Thu, 23 Jan 2025 20:00:21 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-23-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:20714a4d46e54008d5bd9fa24b4f41649675c83127d6463273e07bb3ef2aca61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6204777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734375a0d30c15a2fb6eabfa667a40ac806659307ac669ba13bae90e02e0deb2`

```dockerfile
```

-	Layers:
	-	`sha256:1edb83b2dbe77bdd149c7ef3e1183e9aef8fe312f59b6c136ec9a2dcfb7d4547`  
		Last Modified: Thu, 23 Jan 2025 20:00:54 GMT  
		Size: 6.2 MB (6188267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7fbec69f607bba1fd3aceb56986eb498cc5a7b6e739e3a0c3a3dd4ea577f13e`  
		Last Modified: Thu, 23 Jan 2025 20:00:54 GMT  
		Size: 16.5 KB (16510 bytes)  
		MIME: application/vnd.in-toto+json
