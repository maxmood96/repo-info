## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:070d6f6691327ef3e6d07be0fdf29a141421fbaf0b094ea708b59bf42b7268c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:342197a70f4ae119a0ffaf21200e61c49d65e50fdc7be7444151b15ccb084bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130075000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc87e2b9b75991e62cc2093bb6966738e5102b633f4991080e753941d103fbf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80730a78c02e7159164cfdd9ae2d91a8e6d0a21d3e185160542366050e8fcdf5`  
		Last Modified: Tue, 14 Jan 2025 21:42:38 GMT  
		Size: 76.9 MB (76924525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48b2e4b7be28e8de0ba91e680e7e6a97ce6dd9c0b10b9232d6e67d4fa2336404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057531168e43577c5c1295b75e9f61b37283f33bac5f363549408e16b8f72eb8`

```dockerfile
```

-	Layers:
	-	`sha256:7baab73fa0dce9e56ae306406a259e21af648d77e7dbd23c2188b46873e23b11`  
		Last Modified: Sat, 11 Jan 2025 02:29:17 GMT  
		Size: 5.2 MB (5218593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b2bbe00b09ded2d3512a3b6346c73750ded9b41137dbb01e55a0969632ee5d8`  
		Last Modified: Sat, 11 Jan 2025 02:29:17 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7aba5cad5f9ae63eb7814198f48b688f633e60af44cf962f894e5653cd0a7d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128395566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e41b63d8498bc09c64299989847822f303857556d9c592de984d276434666ce`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6242473a1ca7a3732fdda88ff1ead9baf39ffa44a377f854d9e59621e5854d`  
		Last Modified: Sat, 11 Jan 2025 03:01:03 GMT  
		Size: 76.1 MB (76127370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e68583159b208c70330095b8c73f94d97f39c1e81b4c7ec351ac8a4db4fa64a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5358ff62ef989d82b6b378302dc39ae92fcbb5f70dd42269a57ff9b7bb8b9c86`

```dockerfile
```

-	Layers:
	-	`sha256:420ff577016f018cfa1ee2b7be3968fc3bb38a7de07368b999b5b6f2eb3d74e4`  
		Last Modified: Sat, 11 Jan 2025 03:01:01 GMT  
		Size: 5.2 MB (5218214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8e7f526538992eb2fee8ae58ee1762cf553f63bafb73d6f5bc108ed30f13aa3`  
		Last Modified: Sat, 11 Jan 2025 03:01:00 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
