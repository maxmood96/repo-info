## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:36392c1b3a288fa554e8443043b8dfd31a06dbad76ba7dfb263a09d09a25cee3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c15c957824400ed2ebb57944747edbbc7a41d7e2b73883a202276f2d4a03ff8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.0 MB (136009179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7578f7afa002fe231663a90240689e019a9d8599b3c9c1aa025110a60eb5a86e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a691d620f1b444f47395d9e355a038282abcb79fbc97faf148475e304f5d6bd`  
		Last Modified: Thu, 27 Feb 2025 21:08:20 GMT  
		Size: 82.9 MB (82857446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d4163a8c34833481eb22e3d00d233b873383c8088b7d2d4e1019e1cca0acca9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c37d2b7fdf04080a4f4e78b7d29ed1b4a76171fd8ccde74f63847fb7615558`

```dockerfile
```

-	Layers:
	-	`sha256:2b48730bc525a0090cf4c349b6d6c6362477443c70d5fafbe579a782ad39843a`  
		Last Modified: Thu, 27 Feb 2025 21:08:19 GMT  
		Size: 5.2 MB (5184962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:376683dec82d91725bfd769a63980dfcba5119898c0e0deaf0c03378216760fd`  
		Last Modified: Thu, 27 Feb 2025 21:08:18 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c9d7e52e305b4a925407507efb1fcbca578769744e5d2af3bb8bde2ca92b5ff7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134573338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0857182d85a80b6605c65e56fb87ee7c1f685d08046e78c20117b022859da0ea`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9936c854c12523807d28aef9b7fbc74019bacdc6757c3126c69b31d85c1fd2`  
		Last Modified: Thu, 27 Feb 2025 21:18:06 GMT  
		Size: 82.3 MB (82302068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:821de80bd4b8001c1e52359c1cba3369bc4c26cf42cf5be2dba146652e839b92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9586efb6ae12c8516cf23354e20cbf77a84d1272c57a7a03901c13db8eaed3ef`

```dockerfile
```

-	Layers:
	-	`sha256:4c156df26dacd15d438f99faaa7005d27479a937d5729d03962f43aa80ae7d72`  
		Last Modified: Thu, 27 Feb 2025 21:18:03 GMT  
		Size: 5.2 MB (5183753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0439fc9df51c70a130f6aaa44662ad46fbfa311be264cde07810b6f314cd35ea`  
		Last Modified: Thu, 27 Feb 2025 21:18:02 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
