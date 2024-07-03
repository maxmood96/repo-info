## `maven:3-amazoncorretto-8-al2023`

```console
$ docker pull maven@sha256:486553c329cd281f9b57230466cb4a29c486ff318d246a6b0d0d183e36b8d3a7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-8-al2023` - linux; amd64

```console
$ docker pull maven@sha256:5cc9d1a411c79c620c9a27c2b4f88e22e6897de7cc227704c38cf3fb825f2a54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 MB (391268515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c98d4cbee56aa70af763a3f59482011760692d682b82c9dadd4a0b490d9e4552`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:e6df6db8aef540204b86452a41cadd353e4d48e223134b5e21dfa05ef97e1d88 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=1.8.0_412.b08-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:64c0ea435019c1248fa40e9bf651d8e81c9ad25690c0557bdf9baf369c7fdadf`  
		Last Modified: Fri, 28 Jun 2024 01:20:06 GMT  
		Size: 278.3 MB (278323062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e0eff9e90c77338fa9fc45fd35936b2f2ec7617de1157e2f9438abf6266763`  
		Last Modified: Tue, 02 Jul 2024 09:11:34 GMT  
		Size: 51.5 MB (51462823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ec9f0cfe26eff9a8920ccdc5753016dc8c98469ead2dc711cb4ad56f9195821`  
		Last Modified: Tue, 02 Jul 2024 09:11:34 GMT  
		Size: 9.2 MB (9161814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c3b4374c89c22876388c72ace455bfabe37f47500c79974d26fe254cebbfb0e`  
		Last Modified: Tue, 02 Jul 2024 09:11:34 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e92e21a0005e180835178c70cf3f956cb239bebda910797a7702ac3c6e8374b`  
		Last Modified: Tue, 02 Jul 2024 09:11:34 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:fe7a99a284bff01b5ecbaa13ca8d3198ed8ec1037573cb1f51fc63ca8139fe29
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **12.6 MB (12610674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb04d41779add10a6167996e0a6128d82c097bca24b7bdbb5370a3c5f19a944f`

```dockerfile
```

-	Layers:
	-	`sha256:fc640a606b9bd90b99f20519e3b69dd7b2c38192ef660785b010fd97b2143cf4`  
		Last Modified: Tue, 02 Jul 2024 09:11:34 GMT  
		Size: 12.6 MB (12594421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e6d3abd9ba20891686debd1cd8b533e21a56834bcb6ed54d76d68e939a10642`  
		Last Modified: Tue, 02 Jul 2024 09:11:34 GMT  
		Size: 16.3 KB (16253 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-8-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:74b0a1b620bf8b58e816f947c17f69fe635cc1fbd22fa97717666835c64558fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228681476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2516736ae281d3db390d1ef923737cb3c3d4f49582c2e5817eb08ffda6c94f8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Jun 2024 09:17:07 GMT
COPY dir:e916198a9a0937e23f608a553229a3149679983e31d80cb67d2ef3b5d0279cb6 in / 
# Thu, 27 Jun 2024 09:17:07 GMT
CMD ["/bin/bash"]
# Thu, 27 Jun 2024 09:17:07 GMT
ARG version=1.8.0_412.b08-1
# Thu, 27 Jun 2024 09:17:07 GMT
# ARGS: version=1.8.0_412.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 27 Jun 2024 09:17:07 GMT
ENV LANG=C.UTF-8
# Thu, 27 Jun 2024 09:17:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
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
	-	`sha256:4e77c4c69e4088959e46d4c4f3b1a251af0196d224340f786c9c7a528e097463`  
		Last Modified: Fri, 28 Jun 2024 01:26:02 GMT  
		Size: 118.5 MB (118547427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:589a3b9da4a23541aec9083e2165ad78e877e76f5929f9d2715a80dd97f75a53`  
		Last Modified: Wed, 03 Jul 2024 10:40:13 GMT  
		Size: 49.6 MB (49564134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:974c2b44e48eced3cafd8ef140b6c019a3435084c53c3366838708f7e7cf6011`  
		Last Modified: Wed, 03 Jul 2024 10:40:13 GMT  
		Size: 9.2 MB (9161772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59da814fc39f1ad716786d078d50d2c3c6906d16fe640a33bad6b7cc83d68985`  
		Last Modified: Wed, 03 Jul 2024 10:40:12 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157e1bb12f53987d0afb7ad8a143115eb0d83830dbaa84abeeb387dca5ed6d1b`  
		Last Modified: Wed, 03 Jul 2024 10:40:12 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-8-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:e1d14910def8fdb219fa8adfeb52b821b3fe88b13c5412836c2b05bbeafa2698
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5824101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a02311afd04f9760f731efb86d30d59c430dc9a84619a8453d6d1bcc9d11d9`

```dockerfile
```

-	Layers:
	-	`sha256:81a3b6ae4b5ce3267684f20ed8c104cbf8d86a07273b652c022fb217222cfa2b`  
		Last Modified: Wed, 03 Jul 2024 10:40:12 GMT  
		Size: 5.8 MB (5807196 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aadf109203eca0925b783f9abeecdbe785fba6f0f546a440fbb29e2b44cd552`  
		Last Modified: Wed, 03 Jul 2024 10:40:12 GMT  
		Size: 16.9 KB (16905 bytes)  
		MIME: application/vnd.in-toto+json
