## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:6fbeacb44da845555220968e1a8d0959fb9fcb764e02515b226fdfff9ff09e27
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
$ docker pull amazoncorretto@sha256:0338d9254fc40f4a775c6b4cf1e2c01e257f63e64376f1607ac4ea0938501771
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.7 MB (127679942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14c096b0f01774a72a1b030f8057548a4fe2d8583e227f3cb970d646ddd14a1f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7724834d84abbeddf5cfdf761aeb706df71517910616b754c2f5c144207c2df3`  
		Last Modified: Thu, 23 Jan 2025 18:36:29 GMT  
		Size: 75.4 MB (75411746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9cf5a806597e0972f12ecc12930e4252be20e7ca06c1863d0b71b7d3b110ece3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dbc0df4ad3761b310b76b1457278354eaa539d2225958a7c3dfa5cadcbc9605`

```dockerfile
```

-	Layers:
	-	`sha256:1c1ed66db00bf6f2c3d3391199d45533e1eae7e244cde775e6f85421489fa4fd`  
		Last Modified: Thu, 23 Jan 2025 18:36:27 GMT  
		Size: 5.2 MB (5192965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d7646f4c2ad2599e6734b8ae44ce96d84f896f18c5ceff677ff7abd1b6f697d`  
		Last Modified: Thu, 23 Jan 2025 18:36:26 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
