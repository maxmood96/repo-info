## `maven:3-amazoncorretto-17-al2023`

```console
$ docker pull maven@sha256:3f9af999ae540e22f39df65894d36dc543efb360d27b519b5f0e09a57ef058cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-17-al2023` - linux; amd64

```console
$ docker pull maven@sha256:bd5039defef635d31b844e3d4dc9adb6f674608dfda1e8f65ca26767bbb1d69d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.4 MB (342384511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6f59734dde18952bafc5fa90ec49cb28e05605cc5a93dc8fa6fbe08772543d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:07 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:26:07 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:07 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:07 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 21 Apr 2026 18:11:53 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 21 Apr 2026 18:11:56 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 21 Apr 2026 18:11:56 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:11:56 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:56 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:56 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:11:56 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:11:56 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:11:56 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:11:56 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:11:56 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:11:56 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:11:56 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:11:56 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:008cbcc9cf06909dadd7713e6243b1a02925fac6d3632b00ee5b3c83554fe53c`  
		Last Modified: Wed, 15 Apr 2026 21:26:29 GMT  
		Size: 156.9 MB (156911119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0f5c89df96b588d770cfa61ba516adb405e553a902c7e7039d424d7f631adfe`  
		Last Modified: Tue, 21 Apr 2026 18:12:16 GMT  
		Size: 109.1 MB (109056711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53907b0353dd655d192d54a2fa83748425c7dde774a11e29772aab46893ad883`  
		Last Modified: Tue, 21 Apr 2026 18:12:14 GMT  
		Size: 12.5 MB (12532217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b64c698ef67aa06a9f9087b54a295d51e4821b20ee7268662ca9f932131627d`  
		Last Modified: Tue, 21 Apr 2026 18:12:13 GMT  
		Size: 9.3 MB (9312201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a14014d977ebf989db065cba53feb003bd8c1f1a38a5882a409ee47e4c7384f4`  
		Last Modified: Tue, 21 Apr 2026 18:12:13 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bcc2616e74df845df721a45fe4c325a9cbc7019a2640234943299c02b41e02`  
		Last Modified: Tue, 21 Apr 2026 18:12:14 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:f9add8c17b1147b9d67eecab5df6902d9f33c86709d67750675262c78ee0180a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6254746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e4843577a1c4ef9e0450987ee3e30fae071b59cd2a82695ff7ec3013c12a164`

```dockerfile
```

-	Layers:
	-	`sha256:08183084192bce11c08efa68839748663127c8f234fe3852e32210bb7a8a344f`  
		Last Modified: Tue, 21 Apr 2026 18:12:13 GMT  
		Size: 6.2 MB (6238457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0361097a4273800405b8937dbc39a2ca17e1fc44091ee484ebb49622870289ca`  
		Last Modified: Tue, 21 Apr 2026 18:12:13 GMT  
		Size: 16.3 KB (16289 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-17-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:66a3baf964aef7304b5b236fb4938e997506442d0f7ca1e809d1599fdb2437bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339178188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8d6049ecb56d5ff8085261faa4e946fe8d41412686a3853527b67ae8fc88dd9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:06 GMT
ARG version=17.0.18.9-1
# Wed, 15 Apr 2026 21:39:06 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:06 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:06 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
# Tue, 21 Apr 2026 18:11:47 GMT
RUN yum install -y tar which gzip findutils # TODO remove # buildkit
# Tue, 21 Apr 2026 18:11:49 GMT
RUN yum install -y openssh-clients # buildkit
# Tue, 21 Apr 2026 18:11:49 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 21 Apr 2026 18:11:49 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:49 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 21 Apr 2026 18:11:49 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 21 Apr 2026 18:11:49 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 21 Apr 2026 18:11:49 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 21 Apr 2026 18:11:49 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 21 Apr 2026 18:11:49 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 21 Apr 2026 18:11:49 GMT
ARG USER_HOME_DIR=/root
# Tue, 21 Apr 2026 18:11:49 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 21 Apr 2026 18:11:49 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 21 Apr 2026 18:11:49 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ece4200ddd22a4421c854fc02730d00179c130556075100cac3ac7322df40bb`  
		Last Modified: Wed, 15 Apr 2026 21:39:28 GMT  
		Size: 155.7 MB (155728403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979d9717b9aad50ed021792d841322fcc3d97ffbbe05350d072a8e4e9dcee7f9`  
		Last Modified: Tue, 21 Apr 2026 18:12:09 GMT  
		Size: 107.9 MB (107903732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c67eb942b249cc31087d697345ab78bfb06009ea2ace42ca40f6f769938abdab`  
		Last Modified: Tue, 21 Apr 2026 18:12:07 GMT  
		Size: 12.8 MB (12790059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959b800454903a34c39611ce0540bed976a38bd8778556feff036d3c3e1ab0cc`  
		Last Modified: Tue, 21 Apr 2026 18:12:07 GMT  
		Size: 9.3 MB (9312245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37b09d1cda2a0f37a8021df8d41c2994407edb6a5ed89b1c0b5ff99edb255dce`  
		Last Modified: Tue, 21 Apr 2026 18:12:06 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b48f5039e4a0398448c4a6c0875fce3e0ab00cb7639430485f9e38c47a73942`  
		Last Modified: Tue, 21 Apr 2026 18:12:07 GMT  
		Size: 159.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-17-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:8bcca1a40deae6f5867bac38227a76077ce209681fbadba2c0892cc0e40a845f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.3 MB (6253824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0741e3730fc35a4e7206040e9bdea6d8071b9dbe3135a6d64a1febc4799e5004`

```dockerfile
```

-	Layers:
	-	`sha256:9bac904595bbe54b777cf43f7bad37c176795719c8406038b563e721883a61ab`  
		Last Modified: Tue, 21 Apr 2026 18:12:06 GMT  
		Size: 6.2 MB (6237387 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b27162c68b8f3cc412579aafe8698cbdd06b41010ee8da02409dfb44e6ec5220`  
		Last Modified: Tue, 21 Apr 2026 18:12:06 GMT  
		Size: 16.4 KB (16437 bytes)  
		MIME: application/vnd.in-toto+json
