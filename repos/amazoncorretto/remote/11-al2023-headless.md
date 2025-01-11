## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:72ea614c83c6b26b6e3e0267464ad7097df09b6bfb3a7b41a59d6381e683a506
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4a3933d3e3dbc9998a71413e0778d2b78f7e2004806460411d383fe46c348162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129371208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33b294c899cf8453a9546d846aae8069de2206af5f30f11fac0ef13d86394f02`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:5829ddd7b33103d904f04476a662dc11a662e509c26c675554e66a67426a0dca`  
		Last Modified: Sat, 11 Jan 2025 02:29:28 GMT  
		Size: 76.2 MB (76220733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9be19025f6cb8d9a3c2959736620e1fe1cc6eda5805e860c7abadf24de2834dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a20e91e34a8f95a7698ebfe462493bd04dde1636322e81f270a2048fd80268d`

```dockerfile
```

-	Layers:
	-	`sha256:fb28068e68c9611c6f55ad57a7a5ee1133d302fba3c41678938e04b7ba7e8a6e`  
		Last Modified: Sat, 11 Jan 2025 02:29:26 GMT  
		Size: 5.2 MB (5193347 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:22ba40cdc8db185195450ba971d0487aa6644845a19795a615426ada5f3e8d75`  
		Last Modified: Sat, 11 Jan 2025 02:29:25 GMT  
		Size: 8.7 KB (8652 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:86082cf2c23b475f029d0a8a41405af4b3fd4dfed8a4c4c8082f23ed441b5517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127677957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:699e6efe0c570250e3576f9425449e14a1297c27d524e1018dc1f382c397eb63`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:cd4f5a7980edd394a842506d2c937b5960f250eb1e96caa0c3f0e777d2daa86e`  
		Last Modified: Sat, 11 Jan 2025 03:00:21 GMT  
		Size: 75.4 MB (75409761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61fef5523fede3fe8d633cc7a8ea35dccf2e1e748263abd49c09b81a1bc7ee33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afcf1c7c3d3defabeb6a8468d537a4531633c95b3a42a912b19e6c67518e95c1`

```dockerfile
```

-	Layers:
	-	`sha256:9c3229eafeb7a9ca3db1470e86ac0eb0a4f6ed7dda3ac1a5b09a712aae563602`  
		Last Modified: Sat, 11 Jan 2025 03:00:19 GMT  
		Size: 5.2 MB (5192965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03e18f047c1f9ff1390575cb0f752992adee25c89dbb14905f82cfd4709e7922`  
		Last Modified: Sat, 11 Jan 2025 03:00:19 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
