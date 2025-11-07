## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:c658f4344809554e6c03dc17e059d267ad4c037da67c464abf498baee7db684f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ee13cb147bd9f55f8743603a039d3e582b1c5fcd1b0c1152aa13c6e5752536f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157621067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab6f896c6838f5fd5cabeffd89796b4fbc568bf0cb147abb72e50ca61d05fc1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:15:48 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:15:48 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 23:12:43 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 23:12:43 GMT
ARG package_version=1
# Thu, 06 Nov 2025 23:12:43 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 23:12:43 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 23:12:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:7857af70cc37714ae4781f1d58242c7667f933ef8be05b0636d2c50e756263b2`  
		Last Modified: Wed, 05 Nov 2025 21:09:20 GMT  
		Size: 54.0 MB (54000503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55e3110ed99703f76fa371d2a1f7709e5182add04b94fe2c551cafeceefe3792`  
		Last Modified: Thu, 06 Nov 2025 23:13:25 GMT  
		Size: 103.6 MB (103620564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e363644ee9a575213c652a39925369445ed253470f42e1d3bc84378c9c98509b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7faca55829131470495181893abf763c3411e8b5c418bbe75e3b03a6e6cd9107`

```dockerfile
```

-	Layers:
	-	`sha256:6fb38a93995dc2c2a10cd2b6f9c2e78bf0fd3b3b6a3571883f6194741f7fada9`  
		Last Modified: Fri, 07 Nov 2025 01:51:19 GMT  
		Size: 5.2 MB (5194783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:870f9db0df3ea375050ed7cc5400939da395a178bf272fb740ff072d85f2aa11`  
		Last Modified: Fri, 07 Nov 2025 01:51:20 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:95bb190d0a1066481457046f3033cb6d7bf82c71f24143673a4b8b3d93aec3dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155465073 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67c1aa5b9c7e74061fdde3d3cd05b64ffb91f0e883035ac6b30e33ff46c3ee2b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 06 Nov 2025 22:01:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 06 Nov 2025 22:01:49 GMT
CMD ["/bin/bash"]
# Thu, 06 Nov 2025 22:14:32 GMT
ARG version=25.0.1.9-1
# Thu, 06 Nov 2025 22:14:32 GMT
ARG package_version=1
# Thu, 06 Nov 2025 22:14:32 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 06 Nov 2025 22:14:32 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:14:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:6d0dad3595837e5d244dadb238b6a2012108ea03c6af3e9c48dc16cad05f98d0`  
		Last Modified: Thu, 06 Nov 2025 01:49:48 GMT  
		Size: 52.9 MB (52901684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60e7d6635eb9d30f5b49356144f07079a59548ccd3d120d15fd1cac3242f598`  
		Last Modified: Thu, 06 Nov 2025 22:15:21 GMT  
		Size: 102.6 MB (102563389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6cbc47cd2ff8f6d0d8d6fdbe1b69e17e4fa8b9c2b60d6d0efd0386b835160c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fde8f1ca22a20f898645c6c0b60e09b3e543e723331d57370fd3e8506c1aa7d`

```dockerfile
```

-	Layers:
	-	`sha256:2b73f8f0db5196cefaf3f6855eae73669562a89a93021fe3e7d6e3897c64b6bc`  
		Last Modified: Fri, 07 Nov 2025 01:51:25 GMT  
		Size: 5.2 MB (5193594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:676be593f9f718adf8e7456ce87b94eb650925f721a2117e25460864dca9c5a5`  
		Last Modified: Fri, 07 Nov 2025 01:51:26 GMT  
		Size: 9.1 KB (9122 bytes)  
		MIME: application/vnd.in-toto+json
