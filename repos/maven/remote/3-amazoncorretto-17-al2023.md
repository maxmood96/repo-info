## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:6c16a7e67b2d1eb399da6dddcb6be1bfb2d35c0a3674a3bdfd281badcddf53da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:a36adb4d99115505d3e474d1ce7a6373eff5777d15e6223671a93f46afb7a827
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **268.5 MB (268520163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c6cc4bb7e2029413ff95d9f0dba60eba42426062eb13b9815dd9b592a50742e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:e6df6db8aef540204b86452a41cadd353e4d48e223134b5e21dfa05ef97e1d88 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.11.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:81678b13f6c636072eda0120bcac08ba9702bd3303e400ae3c7400ab681bbeb3`  
		Last Modified: Fri, 28 Jun 2024 00:20:19 GMT  
		Size: 52.3 MB (52319773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba2e9921fd998f4890b7c7984298f249b1ef9d4ecdb3ae8c6b1610a0f4d3c2f3`  
		Last Modified: Fri, 28 Jun 2024 01:23:59 GMT  
		Size: 157.0 MB (157043969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc8c4cf9bdd4655f7c9f91f7f26e0ef2f0e3849f5108477302eeba8e0659d9e`  
		Last Modified: Tue, 02 Jul 2024 09:09:24 GMT  
		Size: 50.0 MB (49993565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6221198e4a0914026ac94b54f362792ccbdb836bfe40532e0c2789eb5a146128`  
		Last Modified: Tue, 02 Jul 2024 09:09:23 GMT  
		Size: 9.2 MB (9161814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e3e08522b6733706599ba72526f3c1e04d0f3bc729055ef4660f70857f0277`  
		Last Modified: Tue, 02 Jul 2024 09:09:23 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf880433bfa1c6b44015adf5becebf521c24776f217ae973a726d40fbab4fe5e`  
		Last Modified: Tue, 02 Jul 2024 09:09:23 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:391829f9143546e1634ec632fbde25e27bf00a7f6bb0022c2e395b9c25d1bdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd4ae8515d788f2ed5b9567322aba8730e5ebf4019a744845557add30e11f0e8`

```dockerfile
```

-	Layers:
	-	`sha256:c412d61cfa90072196f87e0158234735710b9133ba0f26c4be1bdd30ae87f33e`  
		Last Modified: Tue, 02 Jul 2024 09:09:23 GMT  
		Size: 5.4 MB (5432517 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:556f1a87e862fc38ed5a1ead53ab6f3ec900de0cbd5dfca3b6404d75edda7f73`  
		Last Modified: Tue, 02 Jul 2024 09:09:23 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:58c22fee8d99a8482f15d901953f68a1a3d14f04f8fc99381f49e0fe53a763e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.9 MB (265896508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1968eba02f7dd78b1e4e99715c7d4e47a7de152c4a4c7cb4dc207416256a6a2`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:e916198a9a0937e23f608a553229a3149679983e31d80cb67d2ef3b5d0279cb6 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=17.0.11.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Thu, 27 Jun 2024 09:17:07 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Jun 2024 09:17:07 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Jun 2024 09:17:07 GMT
ARG MAVEN_VERSION=3.9.8
# Thu, 27 Jun 2024 09:17:07 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Jun 2024 09:17:07 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Jun 2024 09:17:07 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5e58b9ea919d57f6ca8b1b6a0eab735cb9ec385acc5ae1ab6fb46c492771cb2c`  
		Last Modified: Fri, 28 Jun 2024 00:40:19 GMT  
		Size: 51.4 MB (51407100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1b186d1c65d2a5262edcbb7b2c9ec6fd96a79a0d10bb49c7e144593c5a79a6d`  
		Last Modified: Fri, 28 Jun 2024 01:29:17 GMT  
		Size: 155.8 MB (155750199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d1a13ecc084a88ddacadfeabfdae7399218dc573ed80544b616eeba6f1fc1b`  
		Last Modified: Wed, 03 Jul 2024 10:35:04 GMT  
		Size: 49.6 MB (49576392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:829dcc089c2fb8c937775398735daaf484adf1889a31bec59e3cae44b70d3cab`  
		Last Modified: Wed, 03 Jul 2024 10:35:02 GMT  
		Size: 9.2 MB (9161772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9848526515fc3625501a60c82fdf4e579001eccc4beb3674fb85934259b7d911`  
		Last Modified: Wed, 03 Jul 2024 10:35:02 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b037ba661531e9171661431cfd88dbb096fe65b7be35e2e74885ef67df9a3c9b`  
		Last Modified: Wed, 03 Jul 2024 10:35:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:a6ae2c073fe143d400be4a366a5300304d5232a6ddf93db9917a69936489b2bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5448359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:119a26e5ae869ee4ada46c5e1a40de82d3c8560d483f988e888a3fb22a94fe57`

```dockerfile
```

-	Layers:
	-	`sha256:05be73d464a3a9c4becd11c4e1a6e701fe72e2f4039e2dfa0ca2df11864af24f`  
		Last Modified: Wed, 03 Jul 2024 10:35:02 GMT  
		Size: 5.4 MB (5431443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34c087ce6a7d20b45d7d688ed51cb3b82f6cb5b9e2ba3e5c6e216cde2d3af6dd`  
		Last Modified: Wed, 03 Jul 2024 10:35:02 GMT  
		Size: 16.9 KB (16916 bytes)  
		MIME: application/vnd.in-toto+json
