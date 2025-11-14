## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:59652790dce4df9cffab8b82c8151ed4bff4faa800de093203e4d86ad8f10794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4c95c4caf8ce99e0c1b6fb08f342ca9711456603f0fb7d46203cd38f790da68b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (129963240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa06a381d69a5ea842cdfed9ef2129ba79666ff4923992994aec0a2cec36a333`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:07:30 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:07:30 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:00 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:00 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:16:00 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b64ab808fd6d460065684b4dcddcfaed550a0161a81a4f24db38100a7cef4ade`  
		Last Modified: Tue, 11 Nov 2025 02:45:03 GMT  
		Size: 54.0 MB (53976715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55061baaa358dd328c547553ab9dca2fd1c801f8b84e409adb227ed4d0a45337`  
		Last Modified: Fri, 14 Nov 2025 02:16:27 GMT  
		Size: 76.0 MB (75986525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a14c9e1d5d6069c4fa82d4fa9532d79a94b61333cb50a8e1260e2baeb9dbac20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:696178c62848ac66ca164151267c7fc03657f445445c227c620393261382e738`

```dockerfile
```

-	Layers:
	-	`sha256:1ec0cba7cf94f940ec2ab10e8eb3794e4699d23f6100cf68181b370944bb9f82`  
		Last Modified: Fri, 14 Nov 2025 04:48:23 GMT  
		Size: 5.2 MB (5196819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc75e49c1712d9ee761e35fd06db3421ec5e97d77b7cf174757f9c78677cec5`  
		Last Modified: Fri, 14 Nov 2025 04:48:24 GMT  
		Size: 8.6 KB (8609 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:68fd7e9a767654b6ee9453c78c4c647a5eca3a76cd1dbcc0e259506f9ddbbb94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128093245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46612353b38b14d2d0723e755420448b3c9e33314009f1e13e3691b9e639736`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 14 Nov 2025 01:25:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 14 Nov 2025 01:25:24 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 02:16:00 GMT
ARG version=11.0.29.7-1
# Fri, 14 Nov 2025 02:16:00 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 14 Nov 2025 02:16:00 GMT
ENV LANG=C.UTF-8
# Fri, 14 Nov 2025 02:16:00 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7bff4bcb213fec2224ece2638c720fadc39b0d185d5cfe08391265c58685a0ae`  
		Last Modified: Tue, 11 Nov 2025 02:45:05 GMT  
		Size: 52.9 MB (52876656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dc85c8058bae9fb8d44e5debc9d6c3928138d9abdb7dd0d9e5ca53175357933`  
		Last Modified: Fri, 14 Nov 2025 02:16:31 GMT  
		Size: 75.2 MB (75216589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:03c621269e21a8e379ac7fad0ca602fbcc1f4b0275a2624158dd4fd1509fb430
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b4477a3ea12635f231ae81e5f443cfc124655c18b3474f161886de19deac2d`

```dockerfile
```

-	Layers:
	-	`sha256:feeef473059fe670e6755e756c58551a6d8340b10923b3e755d96e18e856dddf`  
		Last Modified: Fri, 14 Nov 2025 04:48:29 GMT  
		Size: 5.2 MB (5196437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d6b0ad2b241342c24f6478a927ceebdf21c91da8f3442ca3ed0d28e8df67abe`  
		Last Modified: Fri, 14 Nov 2025 04:48:30 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
