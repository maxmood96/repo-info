## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:84e9ab147b128c1e3e04f4c18ce574eed7329608f4532d793ec9a33aedfdef8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:872ebed4c8541fb7869c65bbe5bdd22b5a7f8e93c78b73a60df3e9d7afaa5211
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (135992611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46b39626889d7d8392c6043d63cd438edefe83487cde314072fd3b687b7aab90`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dd6dc3957db7842be985349bc7bfac601e5499a5bc0c59161aef75fd1a09200`  
		Last Modified: Thu, 23 Jan 2025 23:08:10 GMT  
		Size: 82.8 MB (82840076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f97202312d0b89366f17642b7c03968cd1619eb121c3705e274b41929dbe3b8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88fc0ac4990e20b69b02b9b5bb4b4a7b6712f9344bbd7386c982f0493187ab6f`

```dockerfile
```

-	Layers:
	-	`sha256:b834a45e03ef804fd44ca7c6ca8437ff3dd90da1a50bb99cfb1bbb2e2085be59`  
		Last Modified: Thu, 23 Jan 2025 23:08:09 GMT  
		Size: 5.2 MB (5204670 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0486064bc3bdaac39c47a9905fc15104a35e73d15662ff3e77f2f8bfeb0bb9c`  
		Last Modified: Thu, 23 Jan 2025 23:08:09 GMT  
		Size: 8.9 KB (8933 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:473c3ea3c0c438a760f8c58c60012d6e37143476c6e4d429fbf603f4d57f1e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134559686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53819835f419698eacba558805234b491d93248f0e74886f69989b63cd68e975`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:337d1433379cdcb725124dc16dc65f71340fd2fc77635e3ad59f19585a4360bf`  
		Last Modified: Thu, 23 Jan 2025 23:19:01 GMT  
		Size: 82.3 MB (82289487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cf9a54aa8395c1e4929829ffe2d370534ad0ddb1570e0893ec53161484b7efd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660dad8f982477204b4a7c15cbf1d7f805fae3aa858450c0dc17bfc4a1309dea`

```dockerfile
```

-	Layers:
	-	`sha256:293498f9b2cf28f0a025c0d74f7ca7a8da2dee2a7a10825fc39b1bd1473e2e05`  
		Last Modified: Thu, 23 Jan 2025 23:19:00 GMT  
		Size: 5.2 MB (5203461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4abe10504da9864ab388e514793b2cf4a6cbcf293d89e4f883e52e0557f7d15`  
		Last Modified: Thu, 23 Jan 2025 23:18:59 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
