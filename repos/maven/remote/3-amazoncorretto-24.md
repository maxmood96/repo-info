## `maven:3-amazoncorretto-24`

```console
$ docker pull maven@sha256:aec865b097d335847a596715657ba2097bb1db5927503c8aa157e4faaf08a2c5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-24` - linux; amd64

```console
$ docker pull maven@sha256:99c8e2ca46f8303823251027ca47a74d196e17792d667a9fe37d2ce558ae3821
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **329.0 MB (329000622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a7cbae74e70000206e9c1778f98cfd9c1b081c7832459bedbaac259843aa78`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ARG version=24.0.1.9-1
# Thu, 27 Mar 2025 16:03:48 GMT
ARG package_version=1
# Thu, 27 Mar 2025 16:03:48 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 27 Mar 2025 16:03:48 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30e5513f0760ee159f76115f9757d5cbf79408cd7da31a5b6c87b0838e791a07`  
		Last Modified: Tue, 15 Apr 2025 23:56:27 GMT  
		Size: 187.3 MB (187269403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96d3c1983ff7bec3cd5caea4ac5452f8244999faa615fca16bfe2f7e4aee05fb`  
		Last Modified: Wed, 23 Apr 2025 18:11:54 GMT  
		Size: 76.7 MB (76652690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f012984a23bacd942d3a464599fe92a1a2bc352d291d749d69b4ec6220a7109e`  
		Last Modified: Wed, 23 Apr 2025 18:11:52 GMT  
		Size: 9.2 MB (9170432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3020ccdbd22f7e8f39761213d4d06a68af14a01a360acdf604a23e18dc11f2cb`  
		Last Modified: Wed, 23 Apr 2025 18:11:52 GMT  
		Size: 852.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b597e0b2bb186438cf80221a89ddf6acc47f152b178105f0c463717dd9c1dbba`  
		Last Modified: Wed, 23 Apr 2025 18:11:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:a176dcb38a1152073e74fb8bdd399821a31eb4b56115fb628646f13f0593e0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6202786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80443eff3b6edd37c21d4b38d5bac30a97af47c9647a9f85058c42eea0fcc36c`

```dockerfile
```

-	Layers:
	-	`sha256:d92c487bbbc3e307e003bec7c8632e0b3892ef53e91471357a32037e5f34b95a`  
		Last Modified: Wed, 23 Apr 2025 18:11:52 GMT  
		Size: 6.2 MB (6186480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf017c91e74787ca2b9b7bc65f288dc6937ebaa1536dad6b10ea5686ed7b5c2`  
		Last Modified: Wed, 23 Apr 2025 18:11:52 GMT  
		Size: 16.3 KB (16306 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-24` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:8064d9ecc23d69cfafd4bb907dafa2d8780d6cc94de860d98d17d9bc2b329a27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.8 MB (325756903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4a61bedd05198e30af55d32566304e42d26147799a02d8ac2b6dde023fa74ba`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["/bin/bash"]
# Thu, 27 Mar 2025 16:03:48 GMT
ARG version=24.0.1.9-1
# Thu, 27 Mar 2025 16:03:48 GMT
ARG package_version=1
# Thu, 27 Mar 2025 16:03:48 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ENV LANG=C.UTF-8
# Thu, 27 Mar 2025 16:03:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
# Thu, 27 Mar 2025 16:03:48 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 27 Mar 2025 16:03:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 27 Mar 2025 16:03:48 GMT
ARG MAVEN_VERSION=3.9.9
# Thu, 27 Mar 2025 16:03:48 GMT
ARG USER_HOME_DIR=/root
# Thu, 27 Mar 2025 16:03:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 27 Mar 2025 16:03:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 27 Mar 2025 16:03:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f2f51d45657c866ea5cda2cc3fc70c3abf42a75618cd6253edfe6d7f5ab764`  
		Last Modified: Wed, 16 Apr 2025 00:21:33 GMT  
		Size: 185.3 MB (185313497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e3894dbd7baeb41661f22dc74b9c8a355782d805266c04d60868935c083b2fc`  
		Last Modified: Wed, 16 Apr 2025 01:29:02 GMT  
		Size: 76.3 MB (76310932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f9442bace1c7449555fd180202ddb6206e096fd2d4eb5dffa99af749fa4ee27`  
		Last Modified: Wed, 16 Apr 2025 01:29:00 GMT  
		Size: 9.2 MB (9170424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f37566687baa820bc561e49654929ea889e63ab1117eb240d24c47a3af03ac20`  
		Last Modified: Wed, 16 Apr 2025 01:29:00 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd537d494d529a4bfee507d9421a63850e3ee6e7ecebbc10f20a172f95d871f0`  
		Last Modified: Wed, 16 Apr 2025 01:29:00 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-24` - unknown; unknown

```console
$ docker pull maven@sha256:43dd440ebc0bed7528dee709a711d281d438a15747a486ff1cd1a3844778b175
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6201863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:300a78281707b82a8b0ebc0df2801135d04d1090f51dde80bc1852435a326a50`

```dockerfile
```

-	Layers:
	-	`sha256:82518c839f1b0a6fe016094631a34c08e8ff23454d158c9395f54179086389ab`  
		Last Modified: Wed, 23 Apr 2025 21:00:59 GMT  
		Size: 6.2 MB (6185424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b750ef9116d42f4aa2fd55f3693b920adc4d222a01ecfe8c38816c40fda5ff6`  
		Last Modified: Wed, 23 Apr 2025 21:00:59 GMT  
		Size: 16.4 KB (16439 bytes)  
		MIME: application/vnd.in-toto+json
