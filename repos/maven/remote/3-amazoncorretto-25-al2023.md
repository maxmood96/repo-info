## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:f41e8fcd8f4932b64aa85aa70b1708af374c97f900a7551b065f4e12a92e7d2f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:4c143b591ead6eecd0db31dc08c37a520c3428ab8b99c9b1a122c282a38c5a6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.9 MB (363853404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0868d1e13425636ad9a665a358a872ee6ec756c14961d70f35c530ee8a92186b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:24 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:24 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:24 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:24 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 17 Feb 2026 22:30:00 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Feb 2026 22:30:00 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:30:00 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:00 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:30:00 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:30:00 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:30:00 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:30:00 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:30:00 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:30:00 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:30:00 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:30:00 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:30:00 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:30:00 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:30:00 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161b81996e3b0e5e4ba9a4cc5fbc9979cd889a255b08bc1d9d4e0dc355bca0f3`  
		Last Modified: Tue, 10 Feb 2026 18:32:49 GMT  
		Size: 189.2 MB (189187292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40caccc34d606b063e1c40e5d650aa31fbff92eed2c30ca450833356331b581e`  
		Last Modified: Tue, 17 Feb 2026 22:30:18 GMT  
		Size: 111.3 MB (111314611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0434a3fa9587c7585a9154c7bcc7cb8a0f1402b8aded70c5b4646cee645acdb5`  
		Last Modified: Tue, 17 Feb 2026 22:30:15 GMT  
		Size: 9.3 MB (9312236 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7487df6abc01fb2823eca1169455a36ca8d1af4334b92cb52c2d1acfb4a40f3`  
		Last Modified: Tue, 17 Feb 2026 22:30:15 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224e45cf14ada3006837d9cb232b20b54bc50971a04e68a166360fe23519b5cc`  
		Last Modified: Tue, 17 Feb 2026 22:30:15 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:b46abfe93e64d8da1996074e021a1fd57308d31ce005a35d2b5653743ccfc120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9cc0a2796ecc1ae45946c631d2c2104e2f0b8925a84cc1373c88989d01e74ec`

```dockerfile
```

-	Layers:
	-	`sha256:36f7b1cc05ffe921b229b0b066ac577c0f96c2d10aa628b21001f34e5e056cd1`  
		Last Modified: Tue, 17 Feb 2026 22:30:15 GMT  
		Size: 6.2 MB (6207795 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d608f34a1bef2b59755001da36199bc089e9ca6b89e150411288e40807fc03d`  
		Last Modified: Tue, 17 Feb 2026 22:30:15 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:afa0703773b677c897fb134866ba8a0b2acd11028d2e816e9604fc7a32df137d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.7 MB (359745000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:336864d5aa0d6ddc5650d33ff5e274c6d77005c9f046d4e961ac039ccb81b69a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:12 GMT
ARG version=25.0.2.10-1
# Tue, 10 Feb 2026 18:32:12 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:12 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:12 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Tue, 17 Feb 2026 22:18:46 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Tue, 17 Feb 2026 22:18:46 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 17 Feb 2026 22:18:46 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:46 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 17 Feb 2026 22:18:46 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 17 Feb 2026 22:18:46 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 17 Feb 2026 22:18:46 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 17 Feb 2026 22:18:47 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 17 Feb 2026 22:18:47 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 17 Feb 2026 22:18:47 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 17 Feb 2026 22:18:47 GMT
ARG MAVEN_VERSION=3.9.12
# Tue, 17 Feb 2026 22:18:47 GMT
ARG USER_HOME_DIR=/root
# Tue, 17 Feb 2026 22:18:47 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 17 Feb 2026 22:18:47 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 17 Feb 2026 22:18:47 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098ac51664cc3ecb50ec7d80c5020cda656bac5f9d79fc5f5a1093c71586c098`  
		Last Modified: Tue, 10 Feb 2026 18:32:37 GMT  
		Size: 187.1 MB (187088942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d27f1e11c3556a99a294ad9cebbee0ca4500ee7a22e2d23db6514d9018013ce`  
		Last Modified: Tue, 17 Feb 2026 22:19:08 GMT  
		Size: 110.4 MB (110424561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3b32b51c56bf24843fff4429af6831e3d9f644e25a77f92790962ed24139a9a`  
		Last Modified: Tue, 17 Feb 2026 22:19:06 GMT  
		Size: 9.3 MB (9312247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249a66e2343fae1d8fdc271fbd2139361de0a3e843170fe160e514969f8b89c9`  
		Last Modified: Tue, 17 Feb 2026 22:19:05 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ef4e03c93c7a5e916f5a57a3f92b217ecd891e6d8959d996095e06627b4a674`  
		Last Modified: Tue, 17 Feb 2026 22:19:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:1f39d5b7726bbaf2250b13f447071ac7341fdba6e8e1c077aa2dbd64093dca0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6853a213065d24d35df72cbedf775233bdf5c26fb03ca70067e6eaf80c534d95`

```dockerfile
```

-	Layers:
	-	`sha256:52a3b84faa78987f57fd45eb6c80c175857136d6cfa068934bfcde177ee0f575`  
		Last Modified: Tue, 17 Feb 2026 22:19:06 GMT  
		Size: 6.2 MB (6206739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:336fca3219c46abd8b5a548f799fe8264249ea4c3abe61094d1a9450bed8e72d`  
		Last Modified: Tue, 17 Feb 2026 22:19:05 GMT  
		Size: 16.5 KB (16482 bytes)  
		MIME: application/vnd.in-toto+json
