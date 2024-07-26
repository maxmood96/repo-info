## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:a477f1b62464b08115fcae380e6e8004bee14a7b8042d48eeb13b7a05976efd9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:62b698dbebb6c3f13c0591f8f1a6e0c47116e8f77e3b92c29cb7df0a28898727
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141908515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24cbe0908a59326c633b48ebea7b11dc4ff07cdc7f150d933b3dc2f12239502e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f0bdda1f60c020f62660942b81e306de505e01ecada28d7822d3fd76192ac34`  
		Last Modified: Thu, 25 Jul 2024 21:02:25 GMT  
		Size: 89.6 MB (89594336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c4c9213f14cb188041084a174654acc887758bb6392f1afb6e5616d18bfae226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81d1acca027b1d5abc08654c945e4262fabb076d09f03d1de0e337410d688f5a`

```dockerfile
```

-	Layers:
	-	`sha256:ee99270f0015c830782046cf57035426e5acf71d4073cdb0e655db48f6c4c456`  
		Last Modified: Thu, 25 Jul 2024 21:02:23 GMT  
		Size: 5.2 MB (5184961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf7095b8886f5124ecde3f2697a14b8d4175afd0e1b1132cd0a6acb76a322267`  
		Last Modified: Thu, 25 Jul 2024 21:02:22 GMT  
		Size: 8.7 KB (8712 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ead010d7ebf792dfe16ba17b0649284e12b7db5e54c1c3b2b09edd27bc7b180d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140027312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0baf43354f51d11dfc9bc2c3cd7f6f1fff2144f9104881312155404455838ed`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc71d670b3cfd3492373496750be086e9e8c5da067f0e20efacc3bbaeb1e564`  
		Last Modified: Thu, 18 Jul 2024 01:20:58 GMT  
		Size: 88.6 MB (88626174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1bcc526a14e9c4cb9fada6458a8d4671e476439392d94fe797157900c46b2125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c3dffd03de411451378fb6ea6888ecca0008cdb32a7f94b2ab26c38d27751b7`

```dockerfile
```

-	Layers:
	-	`sha256:d64e3eb6841f87c7e2d6ff873e4dd00e900aca462edf9c97911d63e2f9f439f2`  
		Last Modified: Thu, 18 Jul 2024 01:20:53 GMT  
		Size: 5.2 MB (5183749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c1e5c0d715e79401fc7106f96ac61daa70dd5f32f1c5d1f4d7f315329c41e91`  
		Last Modified: Thu, 18 Jul 2024 01:20:52 GMT  
		Size: 8.8 KB (8799 bytes)  
		MIME: application/vnd.in-toto+json
