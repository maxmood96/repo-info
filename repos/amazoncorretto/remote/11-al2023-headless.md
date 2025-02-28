## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a4263680163b1ec9ff64ed1225db3eb7af6f1a00a2b3aded50b958de7236b1f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3fb5944c2548c35f26dcfb85c012ba6ef5d14e8b9d5a8dd72d88d15abca48585
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129389086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759e05835811dba2e3a36fba500b77d31dfa9cce1d2dc5ee713e9c735c105d50`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f332b02855205e16af91ca1c4366245f818ae4ed0d8225976ce342e5f4192a9`  
		Last Modified: Thu, 27 Feb 2025 21:08:09 GMT  
		Size: 76.2 MB (76237353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f4255e62d18566144dcb8b8189b0b5cc6659f0613b910bfdabbaa4b63860c6b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607a274a96ad228ad8b6751615ad52926d1232dc6aa07af390a0d7c657c59387`

```dockerfile
```

-	Layers:
	-	`sha256:251fddab941bb0fd8c27eda1e974659edc5670e5c547988d7a1ec6c7fa4ddcb7`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 5.2 MB (5173639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f681c5f8a62d3f63d066bd402be81b533a185bb74ffdc8127b8a510fcfa432ae`  
		Last Modified: Thu, 27 Feb 2025 21:08:08 GMT  
		Size: 8.7 KB (8650 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:49c7021727c0a1b2341531dc41b415e2f679012da31a623cd82982e41ba029c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127696821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e3dd87718e8019f1351582dcae78bfbab33e301d0889738a91e7d34c2f97270`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47756e09b752b7ed13f74e3144fb3b8b18271ccc0da0a35f701ffd609bef5743`  
		Last Modified: Thu, 27 Feb 2025 21:12:23 GMT  
		Size: 75.4 MB (75425551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:75ff2ce981c48b1079dff7d7b6af041872b20a1e0e579708c3112246b36b5e65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5181989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51c01e7649baf1472e188c4a575846ef5874e5bc9bf5d62f53f84e49c8f97013`

```dockerfile
```

-	Layers:
	-	`sha256:625f0cc62ea997f5ea16eb1179aecfb7eb6b7142da0184327091db493b6a4ad6`  
		Last Modified: Thu, 27 Feb 2025 21:12:21 GMT  
		Size: 5.2 MB (5173257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8275ba9973722f85e32e28aaba4a30f81b051dad0ae0c8588ecb1dcd434f30eb`  
		Last Modified: Thu, 27 Feb 2025 21:12:20 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
