## `maven:3-amazoncorretto-21-al2023`

```console
$ docker pull maven@sha256:92952ba2457b92084c56c94c5c1302a8ee2259cfe9fc49ad06790275fbd98975
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-21-al2023` - linux; amd64

```console
$ docker pull maven@sha256:6b7d986c3aba06e6f9b5a010190902a75d80783390ada6a05688d6ab29d2e0b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.1 MB (282138907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb81b1625c1ebb438f669537fbf1702bc9ba5b20e6eed54ecf9154fc7813243`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:e6df6db8aef540204b86452a41cadd353e4d48e223134b5e21dfa05ef97e1d88 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.3.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:d6eeb694c665f3497df6487a9883dbb0c9b9611ff9771dda8948dbb48516dbd3`  
		Last Modified: Fri, 28 Jun 2024 01:26:30 GMT  
		Size: 170.7 MB (170662360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42beafe6c45981f34a3880487166f4dd7228920784e0f61b5b2e116a038e0cfe`  
		Last Modified: Tue, 02 Jul 2024 09:09:38 GMT  
		Size: 50.0 MB (49993934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc0ff33ced4e680789e38a8b1ebeeaaa2ab36b0cc052e018fbc068eead67fa1d`  
		Last Modified: Tue, 02 Jul 2024 09:09:37 GMT  
		Size: 9.2 MB (9161797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cb4a23e0f86171382d8275602daf70e983e174af0ee1711103d9ac19efb51e0`  
		Last Modified: Tue, 02 Jul 2024 09:09:37 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1d08dd988cf615649563dfe639c5a9750bb5008c5b177020fdc0fb6ac2abc2d`  
		Last Modified: Tue, 02 Jul 2024 09:09:37 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:d7365b0ceef4cc389cbd5e74bdaacce01fa63fe5260229d138ffce63679283d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5452025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36a71033225c655f5a3f8dd5d366ddea41aa911ff5d103ab8e44422d9e443575`

```dockerfile
```

-	Layers:
	-	`sha256:fcab06de9f357232a05ea48612ecfabf0ce65517df66f464a560802e8058b570`  
		Last Modified: Tue, 02 Jul 2024 09:09:38 GMT  
		Size: 5.4 MB (5435762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:734692f9c94d35b144a4b7ce09618cd1bf8048ce14582eca4573728f229f097b`  
		Last Modified: Tue, 02 Jul 2024 09:09:37 GMT  
		Size: 16.3 KB (16263 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-21-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:d55c1e836d2de322d9b292a15af2fa29b099754cb3127da7772a973f25c03eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.9 MB (278945432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606cc1a0ad4be0958bec5cd53d9dbac3208df4058d63299e01841124fa9c022d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:e916198a9a0937e23f608a553229a3149679983e31d80cb67d2ef3b5d0279cb6 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=21.0.3.9-1
# Thu, 27 Jun 2024 09:17:07 GMT
ARG package_version=1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: package_version=1 version=21.0.3.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
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
	-	`sha256:9121cb069e1a3149288eecccee5f05a77e84d8127892d3425230e62b836e9d91`  
		Last Modified: Fri, 28 Jun 2024 01:31:29 GMT  
		Size: 168.8 MB (168799310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b89613eba02bb7ede921116cdb4ab6be2ce48cb282a78a0a3ca0150ba5836657`  
		Last Modified: Fri, 28 Jun 2024 02:09:11 GMT  
		Size: 49.6 MB (49576168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6129d1448d3562085b0daa5aeb63697e09954243f96cb93fa442d86678429ae4`  
		Last Modified: Fri, 28 Jun 2024 02:09:06 GMT  
		Size: 9.2 MB (9161809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe56ae0035e25dae233c2cb913fbea72fce669d96871824792afde021d52f63`  
		Last Modified: Fri, 28 Jun 2024 02:09:05 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b3422eecd0477ce1b1a7d862ccac8d2392fd4f6a7fb03674963703b9a10db4`  
		Last Modified: Fri, 28 Jun 2024 02:09:11 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-21-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:2b24138e8012253d2eb315766f063f7023f31cfe4b5b24f970571b071e9f3e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5451608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94d621ed7d1464a4d4ff03d89c26e207e2dc31b0cf2676e457f9d1c7a4cd0911`

```dockerfile
```

-	Layers:
	-	`sha256:a5f07f7c1ca08c1ba8556f0dcc21e926c27887e4d5eecac825c3743e43e07f3b`  
		Last Modified: Fri, 28 Jun 2024 02:09:06 GMT  
		Size: 5.4 MB (5434692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdabadd455f235fbfee264d49f93b9683b7bba84af431221e302ee5ab12b484e`  
		Last Modified: Fri, 28 Jun 2024 02:09:05 GMT  
		Size: 16.9 KB (16916 bytes)  
		MIME: application/vnd.in-toto+json
