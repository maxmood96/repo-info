## `maven:3-amazoncorretto-11-al2023`

```console
$ docker pull maven@sha256:a66e94258eb028bbfbeae170f87e6fabc45b1b0e144344347161a8220d77353e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-11-al2023` - linux; amd64

```console
$ docker pull maven@sha256:253a964006092c027ef57a0af21c9fe4cce2c5be3fdf946c05a6e9e84c2e3498
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (328995477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c2d97ac9f544506d0160e266ec09fea940b62fc5cdfa61496b16d3727c5cee5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:50 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:12:50 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:50 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 27 Jan 2026 23:14:40 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 27 Jan 2026 23:14:42 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 27 Jan 2026 23:14:43 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 27 Jan 2026 23:14:43 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:43 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:43 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 27 Jan 2026 23:14:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 27 Jan 2026 23:14:43 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 27 Jan 2026 23:14:43 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 27 Jan 2026 23:14:43 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 27 Jan 2026 23:14:43 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 27 Jan 2026 23:14:43 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 27 Jan 2026 23:14:43 GMT
ARG USER_HOME_DIR=/root
# Tue, 27 Jan 2026 23:14:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 27 Jan 2026 23:14:43 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 27 Jan 2026 23:14:43 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87c458a6cbe54075be373b56dd8c2d6eb1d04026358fd8c973d43eb4e51a769`  
		Last Modified: Tue, 27 Jan 2026 22:13:11 GMT  
		Size: 153.4 MB (153367036 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30884b0dfc6245b12f3783a712ef06ffe6be3fe0441342b9ffadc987d28d1f24`  
		Last Modified: Tue, 27 Jan 2026 23:15:01 GMT  
		Size: 99.8 MB (99790517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18f176de18c6d4e9fd78b648322eae9ab5db9c91608d36d2d6d8ec92bc22e547`  
		Last Modified: Tue, 27 Jan 2026 23:14:59 GMT  
		Size: 12.5 MB (12500803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b5dd5056a5a9d81ae21c31e6cd64d1c3fa2982903fae6d3b1c4c3c966ab29c2`  
		Last Modified: Tue, 27 Jan 2026 23:14:59 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fced3325ef203e50b25d0374c408adfbbcae007d0ab2818924e3cef5ee1039c4`  
		Last Modified: Tue, 27 Jan 2026 23:14:59 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f8737c659d93227fb8fb20f85e17a929489958bea91df07185abee3da0698c`  
		Last Modified: Tue, 27 Jan 2026 23:15:00 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:c4db605fecc8611c2016b031c804d9c6a85b1e070182ee0d02f6f67a5a5e6b84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77080e3dcb75e8d9480fa561642fc79ac26281ca5a09ff4293e0915865be5d3a`

```dockerfile
```

-	Layers:
	-	`sha256:304803226ce40f7dcb309c88658c8ed7cd703988425836decbe800e355575daf`  
		Last Modified: Tue, 27 Jan 2026 23:14:59 GMT  
		Size: 6.3 MB (6257535 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d9154bbc59b4ab96176324aa78d3e559bf1a034fb744259636cea1260388124`  
		Last Modified: Tue, 27 Jan 2026 23:14:59 GMT  
		Size: 18.3 KB (18285 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-11-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:86c50e91658b70eb6f90268c62df03c864cdb99f85ab2b3a16a37c4109820e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.7 MB (325713272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:875670b537450c4f43d0d46d26aa27780cf0cdddfc53a3ec52ce40fe1adaad82`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:03 GMT
ARG version=11.0.30.7-1
# Tue, 27 Jan 2026 22:12:03 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-devel-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-jmods-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:03 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
# Tue, 27 Jan 2026 23:14:35 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 27 Jan 2026 23:14:38 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 27 Jan 2026 23:14:38 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 27 Jan 2026 23:14:38 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:38 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 27 Jan 2026 23:14:38 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 27 Jan 2026 23:14:38 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 27 Jan 2026 23:14:38 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 27 Jan 2026 23:14:38 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 27 Jan 2026 23:14:38 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 27 Jan 2026 23:14:38 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 27 Jan 2026 23:14:38 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 27 Jan 2026 23:14:38 GMT
ARG USER_HOME_DIR=/root
# Tue, 27 Jan 2026 23:14:38 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 27 Jan 2026 23:14:38 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 27 Jan 2026 23:14:38 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e6251ebb83330e0c58d2249a2ac20505f88ca1103b17f485ce1964ae06ab697`  
		Last Modified: Tue, 27 Jan 2026 22:12:24 GMT  
		Size: 151.9 MB (151921781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c41a427c2fa50c2ea73422455fe73e1d857e2ac7df2d6eb439973e83f3208f`  
		Last Modified: Tue, 27 Jan 2026 23:15:02 GMT  
		Size: 98.8 MB (98797402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eab776aea79cd89d899be5e05b7f1cd3942cb599315cc66f716b35c18f4e4a70`  
		Last Modified: Tue, 27 Jan 2026 23:14:54 GMT  
		Size: 12.8 MB (12764166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8915b0110129c3bd99b1538b2d180783dbf448db90e894b1f3218a2e14893cc`  
		Last Modified: Tue, 27 Jan 2026 23:14:54 GMT  
		Size: 9.3 MB (9312241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05da9a9fbf7eeb47d4b563f340f8a0cfadc8434f630d09343b360e7200a15f66`  
		Last Modified: Tue, 27 Jan 2026 23:14:54 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fe3f51b3dcf537c451afe85aa6e8d7a24835a46e6bf37ebf5e74f005f3a3b0`  
		Last Modified: Tue, 27 Jan 2026 23:14:55 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-11-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:604ba15ca96970bb7c16d478f7cf0b57068546837444b0b7df8d688bf1df9501
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6275742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:004f7140ecbde8ba7fa84d091a09f34475f8461f5fd4e1d2d22f92404716be90`

```dockerfile
```

-	Layers:
	-	`sha256:f045c6990d3148c5a284a4480ab62a5b3233e736a83177491e51415f1fb65f72`  
		Last Modified: Tue, 27 Jan 2026 23:14:54 GMT  
		Size: 6.3 MB (6257309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7584485395fc9662231dc6f1951a68fe6163fad7f68b795926b14421518b35bf`  
		Last Modified: Tue, 27 Jan 2026 23:14:53 GMT  
		Size: 18.4 KB (18433 bytes)  
		MIME: application/vnd.in-toto+json
