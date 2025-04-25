## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:86a619105952fd3396eb9628de968063ab727bc917022bfc81030a4182271a54
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c0abc78b18a82f2effc9fc6e17c18bef30f2af719eaf7d08aeb820ca0a978874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.0 MB (145000275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e45d2ec07bc80326015ac0d6d3a0c5f51a077ea5c98562adf9bf14b516d75414`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1cf9fb914831ab202ad1756fe44227d7c88c49394a5cc9749ad863e76989673c`  
		Last Modified: Thu, 17 Apr 2025 22:49:09 GMT  
		Size: 55.9 MB (55906521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccf0f908688b42fafdead0c570a99e4aaf8127b89e7c22cbe2d92a8c7eb2262d`  
		Last Modified: Thu, 24 Apr 2025 20:08:15 GMT  
		Size: 89.1 MB (89093754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ad2d7af60de5bdf025ccacc92f592ef657f6bc4ddd5a36df85a88e0ed00f62a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5436142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1703a82554e10d87110fed375cf3fa60eea02477a5effbeb7f66989afedf807`

```dockerfile
```

-	Layers:
	-	`sha256:afb5b2a61a6d5578c70ef360136ba15155a08c97c356aa8ba4f1a49457abedd5`  
		Last Modified: Thu, 24 Apr 2025 20:08:13 GMT  
		Size: 5.4 MB (5427394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c09bd177f9f09ffa6415669fa70116f3c5dde072cdcd33975089abe0bed74435`  
		Last Modified: Thu, 24 Apr 2025 20:08:13 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ca3c9cc7f081894645f809162a41f2d26c7281654eb9d8312b3987417630948c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143202366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc654d4a0b05b5421340a73e9e6c271ec7d5b9e10a6295f6a3f19d3fbc3fb6b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:3851c1e87439f4d250c3c0908923968a64dd743e1e5cfc05b798a52dc5d1e215`  
		Last Modified: Thu, 17 Apr 2025 22:49:07 GMT  
		Size: 55.0 MB (54961479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a14e85368ad3226f3597550fadd676bcfc7a8f268d6d3a77b4f2f8f332b64b`  
		Last Modified: Thu, 24 Apr 2025 21:23:10 GMT  
		Size: 88.2 MB (88240887 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b692a983be727dc11972fc1ccaabf22fcef847e4160e4932a1e52804d8f55997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bae030bfc13e504c1722bec12d8509661183af3d96bdc5b64952abe6aa3c3f`

```dockerfile
```

-	Layers:
	-	`sha256:5c4ccdbfc842a9d75c9e9e8ac5a64bfd189f18e50cbe03bdff459f3cbb81ca9b`  
		Last Modified: Thu, 24 Apr 2025 21:23:08 GMT  
		Size: 5.4 MB (5426184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d9bb3abe709c624da7397ff7e443de1dbbf74934742f56da1e8d20c85fd2e0e`  
		Last Modified: Thu, 24 Apr 2025 21:23:08 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
