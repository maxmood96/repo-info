## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:3f1d721cddc1ff78d4fb808ab4b3d1bffb09294c7b12779e9165f4e9e9c23344
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0dac0d56fd3f55e95efc46f79c0f0326eef963f93e8d2185265ad56c9245da44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134755365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:965b2d3bf5b895e15d26af895b75d47b3c46c9b12f217a1cc428de17bc4450ef`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Jul 2024 20:01:54 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Jul 2024 20:01:54 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f03636e672ba797137f2f72e64c7fdf7947397c0880ca5f9e9962a85462a7875`  
		Last Modified: Thu, 11 Jul 2024 02:05:27 GMT  
		Size: 52.3 MB (52313836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:741800110605712a250a0a8cb45a3f0e3a23b5e69fdb3049fbdd222f579c9b5d`  
		Last Modified: Tue, 23 Jul 2024 00:07:40 GMT  
		Size: 82.4 MB (82441529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f852c3cd3927c2798adbc8b7e3f9452d033b40a4d6baca89ad4b512a1e2342bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:812f7fba3c454cad7e26bf0837abe7a3cf4f4ab8c43ae4815fae75a05df5cb8d`

```dockerfile
```

-	Layers:
	-	`sha256:e547be5c236f77d4797067b965de2ba214f21166e404eea098a23a38f7015aa9`  
		Last Modified: Tue, 23 Jul 2024 00:07:37 GMT  
		Size: 5.2 MB (5182513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:133b5c01af28afd6656f42eddd5c8e895a519a8b26a0d83a7df503c38dc78c91`  
		Last Modified: Tue, 23 Jul 2024 00:07:37 GMT  
		Size: 8.7 KB (8717 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:84b1a9b20012d2209c55677f91cdfe37c5e19bdeda6a85890a7fe59831f26593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133165442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8395c11337c027b2cb90c07b29f3c269e8115a7ab396fccc2027383d2b228030`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:562fcdb1d0b4dfe589c27598faf51b80e7ea6a506df0dbf54b1d19c29db60397`  
		Last Modified: Thu, 18 Jul 2024 01:11:57 GMT  
		Size: 81.8 MB (81764304 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e50e44576f8bf10057a5962107baa0516f5a844882030f9b5dfb062acf68aa4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08688a2e8e6686322126e342d0cf353baa084b6975d64c2a52150eaf28a9d7d5`

```dockerfile
```

-	Layers:
	-	`sha256:12f78bbd0b24da0c3d41016954604ff887615f0bbfef6e80d4cdbc017edeb501`  
		Last Modified: Thu, 18 Jul 2024 01:11:55 GMT  
		Size: 5.2 MB (5181298 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c605242b305547ffa217fda7bd99eb0f9637124874ad6e964a4ebda195eb3a8f`  
		Last Modified: Thu, 18 Jul 2024 01:11:55 GMT  
		Size: 8.8 KB (8802 bytes)  
		MIME: application/vnd.in-toto+json
