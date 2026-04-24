## `maven:3-amazoncorretto`

```console
$ docker pull maven@sha256:34bc70472c811fd05b4fce8071685a76b974148a9997e6e2b14a61044f3f40fb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `maven:3-amazoncorretto` - linux; amd64

```console
$ docker pull maven@sha256:ff65ae1468a7dde7c6b5c7cf925e69b9157fbffff11756b07cb23361b1706675
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.3 MB (374313263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bd02d659ad5ec133ad7111692a5f7cf37ae37afd8b5edd62d70a47a42c330a3`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:07 GMT
ARG version=25.0.3.9-1
# Fri, 24 Apr 2026 00:13:07 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:07 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:07 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 24 Apr 2026 01:14:30 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:30 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:14:30 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:14:30 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:14:30 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:14:30 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:14:30 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:14:30 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8528f219ca74c91c07fe9d908755732a5ad05bb1b1ee9e6170b190b33c7a4e8f`  
		Last Modified: Fri, 24 Apr 2026 00:13:31 GMT  
		Size: 189.4 MB (189412101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b77d9c918cd83d64db4fea806298e73df05a3538ddeb90e710500b59d3bcca`  
		Last Modified: Fri, 24 Apr 2026 01:14:47 GMT  
		Size: 121.0 MB (121018229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe42eb0cffa250771463b3980dc3f68e1d7136e4515baf48533585ad8b74e29`  
		Last Modified: Fri, 24 Apr 2026 01:14:45 GMT  
		Size: 9.3 MB (9312216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a9db6e10f37b989b26fc454e1847c34873bacb98e4388b302e25af266606a1`  
		Last Modified: Fri, 24 Apr 2026 01:14:44 GMT  
		Size: 854.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30f0bf633bc982f37e8558b7def267093fdcc8434debd5d8f09072fa04332e4`  
		Last Modified: Fri, 24 Apr 2026 01:14:44 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:7f04606be173a085c6e8486718da1b297ef3e79ab97cdb1e24821f12600d90bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eed467021ea5e1d7c15351fa7c628ef0d626b61a9d9475c43b545ca1a608c4`

```dockerfile
```

-	Layers:
	-	`sha256:47aef34dd4e32622b7ca1a066b301af1ab2e7af0da379bdb3932cd8dfeec358d`  
		Last Modified: Fri, 24 Apr 2026 01:14:45 GMT  
		Size: 6.2 MB (6216268 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee1b82486adbdc78e52ecdaecb56392a62ac79287c52a2e7717b99a8465c6beb`  
		Last Modified: Fri, 24 Apr 2026 01:14:45 GMT  
		Size: 15.7 KB (15710 bytes)  
		MIME: application/vnd.in-toto+json

### `maven:3-amazoncorretto` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6f274f00c8323ac3476dfb743757770adb2057336be4085eaad91197e14d9a6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **370.1 MB (370138977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69c4b8d458a85b70c7ff8dba28ee749951099f0547703111083cd303e3447e2e`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:57 GMT
ARG version=25.0.3.9-1
# Fri, 24 Apr 2026 00:13:57 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:57 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-devel-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-jmods-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:57 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
# Fri, 24 Apr 2026 01:14:48 GMT
RUN yum install -y openssh-clients findutils # buildkit
# Fri, 24 Apr 2026 01:14:48 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Fri, 24 Apr 2026 01:14:48 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:48 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Fri, 24 Apr 2026 01:14:48 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Fri, 24 Apr 2026 01:14:48 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 24 Apr 2026 01:14:48 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Fri, 24 Apr 2026 01:14:48 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Fri, 24 Apr 2026 01:14:48 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Fri, 24 Apr 2026 01:14:48 GMT
ARG USER_HOME_DIR=/root
# Fri, 24 Apr 2026 01:14:48 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 24 Apr 2026 01:14:48 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 24 Apr 2026 01:14:48 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1deaf9388f856a5d93d551a1645d6107c5b1552a8f7f8a454a18dba1f77d940d`  
		Last Modified: Fri, 24 Apr 2026 00:14:25 GMT  
		Size: 187.3 MB (187330076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a20a284119d8e190eb162a708a37c8442ee7d534206cb19b6bd47d8b987577`  
		Last Modified: Fri, 24 Apr 2026 01:15:09 GMT  
		Size: 120.0 MB (120043386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b00e002c781caf09e8757f65b091d718a41c106a8e8135237755ec95220b06`  
		Last Modified: Fri, 24 Apr 2026 01:15:06 GMT  
		Size: 9.3 MB (9312251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc7c37f782140f6da3519640bbbfad56f4856a6c032cc5d693dadb71c025373a`  
		Last Modified: Fri, 24 Apr 2026 01:15:05 GMT  
		Size: 853.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ab6fd2279c53c1266b7cea79effb75581bbbb0e08bcd6ea74d08c3bfffa9c6`  
		Last Modified: Fri, 24 Apr 2026 01:15:05 GMT  
		Size: 158.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-amazoncorretto` - unknown; unknown

```console
$ docker pull maven@sha256:aabc3c80aa55bb4bf35dbaaac63ec6aa6fced9d77292fcb20abf2a7962bc6f41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.2 MB (6231152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04cf470cc0622155e03e6f8bc0738a9ab0dc9f8d926a4919198f4d9191f5cfee`

```dockerfile
```

-	Layers:
	-	`sha256:04d0129678d13054a3effa3ef773920437c492a3106b4a7def1c93784a85d52e`  
		Last Modified: Fri, 24 Apr 2026 01:15:05 GMT  
		Size: 6.2 MB (6215261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea28ac742a21e72aa7cea85770beb5c877bc5c3a68051b0ea7b0c1851feed08c`  
		Last Modified: Fri, 24 Apr 2026 01:15:05 GMT  
		Size: 15.9 KB (15891 bytes)  
		MIME: application/vnd.in-toto+json
