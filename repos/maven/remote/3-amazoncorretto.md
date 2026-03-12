## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:ae901d7e3696840df66301794bcac5e2386eb2d8faff620c4d1fca94870836fd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:a326f4b55f0ed594667deb9006c0a1f2708855f07ec2ade88714adebf48c6744
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **367.9 MB (367867703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be8c3b15d415003edbefec7661490f3f07b65d6684f757b0f66d9267a08da1e8`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:25 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:25 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:25 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 12 Mar 2026 20:13:42 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 12 Mar 2026 20:13:42 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:13:42 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:42 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:13:42 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:13:42 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:13:42 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:13:42 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:13:42 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:13:42 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:13:42 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:13:42 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:13:42 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:13:42 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:13:42 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1899f99dbf61d2e92bf9bc374b2f4ec7c5b8a1687b8543b4ecc212164833f14`  
		Last Modified: Wed, 11 Mar 2026 18:34:50 GMT  
		Size: 189.2 MB (189186371 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f50b9a5a7c6e68dd6abe516f5fd9cf6f7ac314ad84d748bff1e6c92ffc2aac`  
		Last Modified: Thu, 12 Mar 2026 20:14:01 GMT  
		Size: 115.3 MB (115336015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a82e0fab177d0a5abb7a8478339c4e082e8fc8ae951b7628074e0048bb8cdcc3`  
		Last Modified: Thu, 12 Mar 2026 20:13:58 GMT  
		Size: 9.3 MB (9311187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb50310c6fcef700d0a2c8edfd66d6d9c41b724143118507e49d32461ac7c47d`  
		Last Modified: Thu, 12 Mar 2026 20:13:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fdf3e6c1286a0a01fb8308d45c97c38a07fb66db54f24b18f11f430bce60ab`  
		Last Modified: Thu, 12 Mar 2026 20:13:58 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:702dc77f4ca8d48b118943d9902b0e784ba10dca80fc98ea2062b4e49758eacb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6226634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24ebe5b81ce94d580a1e9ccb79ecd74933ba7bb08797f0e755bc76456b937eee`

```dockerfile
```

-	Layers:
	-	`sha256:f3987477d27ac7922c68e0e6f38328e3778768f52249cce714f367120b8bad1d`  
		Last Modified: Thu, 12 Mar 2026 20:13:58 GMT  
		Size: 6.2 MB (6209085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bf5cb039431f2269627f7696d02378cccaaca3f6e8a331b866fb2f9765c794e`  
		Last Modified: Thu, 12 Mar 2026 20:13:58 GMT  
		Size: 17.5 KB (17549 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:58ed2568f4c3ecababad3eda554346aa14788f95e5bf19d2d9a6e9df7b2de76f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **363.7 MB (363690911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8249f9b7019abd390ebeb75d9367c697f57dc49c274610a6a29339e7c2d503a9`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Wed, 11 Mar 2026 18:34:05 GMT
ARG version=25.0.2.10-1
# Wed, 11 Mar 2026 18:34:05 GMT
ARG package_version=1
# Wed, 11 Mar 2026 18:34:05 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 11 Mar 2026 18:34:05 GMT
ENV LANG=C.UTF-8
# Wed, 11 Mar 2026 18:34:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Thu, 12 Mar 2026 20:12:34 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Thu, 12 Mar 2026 20:12:34 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Thu, 12 Mar 2026 20:12:34 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:12:34 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Thu, 12 Mar 2026 20:12:34 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Thu, 12 Mar 2026 20:12:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Thu, 12 Mar 2026 20:12:34 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Thu, 12 Mar 2026 20:12:34 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Thu, 12 Mar 2026 20:12:34 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Thu, 12 Mar 2026 20:12:34 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Thu, 12 Mar 2026 20:12:34 GMT
ARG MAVEN_VERSION=3.9.14
# Thu, 12 Mar 2026 20:12:34 GMT
ARG USER_HOME_DIR=/root
# Thu, 12 Mar 2026 20:12:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Thu, 12 Mar 2026 20:12:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Thu, 12 Mar 2026 20:12:34 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d9ab420359a2ce38b24b838a3ea4b4bcbfe85a0c06909eead4a8cca721947cb`  
		Last Modified: Wed, 11 Mar 2026 18:34:30 GMT  
		Size: 187.1 MB (187088807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86acde7ab1b8db2152f905250f08eee97df4c4d190555dd81d1960590ddac591`  
		Last Modified: Thu, 12 Mar 2026 20:12:54 GMT  
		Size: 114.3 MB (114348514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ebfafa9d251519bc824f098804f7812bca3da0b25b0c93de8d6c02028fc803c`  
		Last Modified: Thu, 12 Mar 2026 20:12:52 GMT  
		Size: 9.3 MB (9311176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51ba945c41251fa3a9d0bb8f49ca7ca9332d70f6c4175166dcc347e7302844f7`  
		Last Modified: Thu, 12 Mar 2026 20:12:51 GMT  
		Size: 849.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cd3f0ebba74a4292621c2a151b9e3057563dc42b571e594267fb22d2e885c4`  
		Last Modified: Thu, 12 Mar 2026 20:12:51 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:f958ebee325ab5077aa9a103064939d420642d58728869573969dd5a5dcb204b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6225807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ba4b00870d6c66c8a4fa41445a653bb8380b880da974fb8af0aa06cfd6e036`

```dockerfile
```

-	Layers:
	-	`sha256:d939ff1dda54fd6685ef21c6c5ce4c8b378a0d0ed3ce50badf14fb5a12733af4`  
		Last Modified: Thu, 12 Mar 2026 20:12:51 GMT  
		Size: 6.2 MB (6208077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728ad0849d8ce864e55621e17e3f2240c1cba6e6bf9663e87149e9fe9b65d02e`  
		Last Modified: Thu, 12 Mar 2026 20:12:51 GMT  
		Size: 17.7 KB (17730 bytes)  
		MIME: application/vnd.in-toto+json
