## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:905a609b9894972ba1e3d8f299df420f93ca6cf8a578fcbc5e44b3959b6edf63
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:aa4c856171c0bc0130f97ed0e4ab9bed070cc8c10c38c88d641a4e46e1eb4cd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137117448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b8630535f9ac25bb59875f4875ae982d3ff9dca44a88dd3e5d64a3566c450b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:35 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:31:35 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:31:35 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:31:35 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3c5ac15e3b3125c640c298978d292eeecad886acc383b063ce80ae9f07a8c5`  
		Last Modified: Tue, 10 Feb 2026 18:31:50 GMT  
		Size: 83.1 MB (83079220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e579cef4c8c2b6a4cc151a42482bf3134698820a85e8d185c94e7642088ac4a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fefbf44ce96ec046c15c5d268823cf8683634ecbc657b1dc8491bf0a28b472`

```dockerfile
```

-	Layers:
	-	`sha256:305a857ca5756847d9fd4a6ce034d42727ec5c3ae37e81d475a30dcfd869bcf5`  
		Last Modified: Tue, 10 Feb 2026 18:31:49 GMT  
		Size: 5.2 MB (5208325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee9e5e65c4c36f674904ee26e291b87fa60f22ac088fed3a0bbd97255ce3b39d`  
		Last Modified: Tue, 10 Feb 2026 18:31:48 GMT  
		Size: 8.9 KB (8891 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:002d23d46c7bf29be47c8c9f712c13e32a2d4b549d75a68a8bf97c317f791bdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135412489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aeec624d094bcc087cba8dd6c3cd60ac7732fa00c91e65938d356b781d1e6cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:27 GMT
ARG version=17.0.18.9-1
# Tue, 10 Feb 2026 18:31:27 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:31:27 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:31:27 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3242122167900c530f5ec73743fa8f94f6a42f9d3906bfee097a4a5daeeb7b`  
		Last Modified: Tue, 10 Feb 2026 18:31:45 GMT  
		Size: 82.5 MB (82494278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fee705f182941da3ab3eabcb34b9caf9b94cd015bd58a1e40f147aeb688ef8e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b2e63ff602f3f5cdaa502204cb1c39803b9dcd0f1bf176cb3a843a7b9498a5f`

```dockerfile
```

-	Layers:
	-	`sha256:ad178d0376dfd0f96ac424e126395fa3a92692b8254034ef2969499b07dfbfce`  
		Last Modified: Tue, 10 Feb 2026 18:31:43 GMT  
		Size: 5.2 MB (5207116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a12e6a6a0fbf18ac49398e10e4ea61acc14f8f6ae7f6492f022a5afb9a9c163`  
		Last Modified: Tue, 10 Feb 2026 18:31:43 GMT  
		Size: 9.0 KB (8971 bytes)  
		MIME: application/vnd.in-toto+json
