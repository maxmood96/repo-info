## `maven:3-amazoncorretto-25-al2023`

```console
$ docker pull maven@sha256:4870fb45f2f4c7dcab1cee45ef919073fbeb7f413341116844bdf63abb5338b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto-25-al2023` - linux; amd64

```console
$ docker pull maven@sha256:00a1f579ae3e41ac09a05f91a5b99da64f8ccb94439df33611d01ae51e2b35ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.2 MB (358161066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3711f559dcf09959026498b286f27cc31c3819fa3cb19baa23104f7ebe12f9a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:21 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:21 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:21 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:21 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 17 Dec 2025 20:09:12 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 17 Dec 2025 20:09:12 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:09:12 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:12 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:09:12 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:09:12 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:09:12 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:09:12 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:09:13 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:09:13 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:09:13 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:09:13 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:09:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:09:13 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:09:13 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91413819017580b0cad6a6036474dd8d9101d5528fc612f3e8b639ab91f6de1b`  
		Last Modified: Thu, 11 Dec 2025 22:17:29 GMT  
		Size: 189.1 MB (189138728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53218867d6c319d52aaf0b45756021761838cabca12ccb189556ef2c7a7f14f5`  
		Last Modified: Wed, 17 Dec 2025 20:09:53 GMT  
		Size: 105.7 MB (105720594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fa9272ae10ee3097c0a4b4bf27d28a7c3bdf24f888c81de32ab6a2a6ac5ca1d`  
		Last Modified: Wed, 17 Dec 2025 20:09:38 GMT  
		Size: 9.3 MB (9312243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:435eba3b49ccd9bcd9ef81b2eb1ee86b86dae8919b3b49fdc91e170f165ab945`  
		Last Modified: Wed, 17 Dec 2025 20:09:38 GMT  
		Size: 851.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f6d24e67bb7fdc0d9c906cdb307e65fdfba8d6e9ec6d7de25b5e8bca7b08b2b`  
		Last Modified: Wed, 17 Dec 2025 20:09:38 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:9daa53e2824638c4bb3ac888023e5f7b1740c39dbe00da03ab8fc33913d344da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6224131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cc6341a82dc976e9c56ae85374d262444db51d6312248e3c45f5e0a2168837f`

```dockerfile
```

-	Layers:
	-	`sha256:07788679e02a987f7ae49e35748b4d6198416d868dc11e02a945307c4ebee034`  
		Last Modified: Wed, 17 Dec 2025 21:29:42 GMT  
		Size: 6.2 MB (6207781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:007249fdcba76e21380c62ed535cb13ed95aaf09605876d15313a21d946a94ec`  
		Last Modified: Wed, 17 Dec 2025 21:29:49 GMT  
		Size: 16.4 KB (16350 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto-25-al2023` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:f25cf9bdaacdee036fd46e382276625aa1642f40af913bc83cbc475be0edbcb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **354.3 MB (354271029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c290d7756ade99e6ca542a731e0bae2a6ff1cdea79879b76fc48e09a4c13c04a`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:00 GMT
ARG version=25.0.1.9-1
# Thu, 11 Dec 2025 22:13:00 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:00 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:00 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Wed, 17 Dec 2025 20:08:59 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Wed, 17 Dec 2025 20:08:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Wed, 17 Dec 2025 20:08:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Wed, 17 Dec 2025 20:08:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Wed, 17 Dec 2025 20:08:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 17 Dec 2025 20:08:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Wed, 17 Dec 2025 20:08:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Wed, 17 Dec 2025 20:08:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Wed, 17 Dec 2025 20:08:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Wed, 17 Dec 2025 20:08:59 GMT
ARG MAVEN_VERSION=3.9.12
# Wed, 17 Dec 2025 20:08:59 GMT
ARG USER_HOME_DIR=/root
# Wed, 17 Dec 2025 20:08:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 17 Dec 2025 20:08:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 17 Dec 2025 20:08:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ddfd06178dcdca2a5cd3684d7be72c33b03527be5f3cd9c8aa6e0db1f16ac0b`  
		Last Modified: Thu, 11 Dec 2025 22:35:49 GMT  
		Size: 187.1 MB (187059439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6138f4e8d38a25cd69dbe0bcbd74233e790f659662a3beea3b841392cba31407`  
		Last Modified: Wed, 17 Dec 2025 20:09:42 GMT  
		Size: 105.0 MB (105024851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9907a5e3424ea96d7ae7d39ce293c9346887d3db70e3df03712e3ec59ea295e`  
		Last Modified: Wed, 17 Dec 2025 20:09:26 GMT  
		Size: 9.3 MB (9312248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b3c9247c80b1321e0c52ea23c553729103158b67289e8a968d09b6f6bfe7095`  
		Last Modified: Wed, 17 Dec 2025 20:09:25 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 09 Dec 2025 23:54:32 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e31f0111580d4a4e2f366a792ccd84e76b460d0f07dd74a644a42205c1ba979`  
		Last Modified: Wed, 17 Dec 2025 20:09:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto-25-al2023` - unknown; unknown

```console
$ docker pull maven@sha256:38ea34f717b00797c20ca0c037df93d324f7fbc28b300bb19d2066120eb73b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6223208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10959df8ec72613b616bb7845749443a5bdcf9ab53bf55bffc9947eafdf578f4`

```dockerfile
```

-	Layers:
	-	`sha256:7c5da43b8540d72231464761d03926bf9acbc9a2db55e1295dd2012af6b5957e`  
		Last Modified: Wed, 17 Dec 2025 21:30:00 GMT  
		Size: 6.2 MB (6206725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec06d6d7800d5b75dae02780f033d6a0989574c9b881ac335271cd81bf83607a`  
		Last Modified: Wed, 17 Dec 2025 21:30:01 GMT  
		Size: 16.5 KB (16483 bytes)  
		MIME: application/vnd.in-toto+json
