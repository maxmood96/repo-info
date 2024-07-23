## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b19e2def2a4e48197bbcd79615e4a0751560e2b0817841ee4358cbb683beaecf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:77f0b9a246e8062bb0a942a477063e2172091c1ab55c24ec9e8b160370f93695
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141908091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbceafce50071dd5a65fb7b14233968d7b9c8e4b47e628e849598543b561def1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Jul 2024 20:01:54 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Jul 2024 20:01:54 GMT
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
	-	`sha256:f03636e672ba797137f2f72e64c7fdf7947397c0880ca5f9e9962a85462a7875`  
		Last Modified: Thu, 11 Jul 2024 02:05:27 GMT  
		Size: 52.3 MB (52313836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96013f93a57ffc166bc43619636abe343068bf039ddfb7608a7b0707d0cf28d1`  
		Last Modified: Tue, 23 Jul 2024 00:08:43 GMT  
		Size: 89.6 MB (89594255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f5846a1868539a47a193888bed7a8c6a3a1a73b0d2b159559bf5a561949b6798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf5fcf29e000feb4829b6b2892106b785a591a39e998262cf0b0906e1a43603`

```dockerfile
```

-	Layers:
	-	`sha256:10214159388666c82a3847a048df5cf65e93ef49109d71bdbb81b2e7bc04fce2`  
		Last Modified: Tue, 23 Jul 2024 00:08:42 GMT  
		Size: 5.2 MB (5184961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be20346ee900dbe1c46323ce94d918cc1d6e8907b9d36deb370c6b0c28ba6fe8`  
		Last Modified: Tue, 23 Jul 2024 00:08:41 GMT  
		Size: 8.7 KB (8714 bytes)  
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
