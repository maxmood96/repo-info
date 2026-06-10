## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:7ff562deddbf874c0249a6ba49e827662c9758af6853176ee445eb0e5cb184d3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2b220d8889eed108e061e58f1c38dae1638cfbd65f86dcbfd9c344c1910fff31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130629703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cfc25fcaf61b9a1bae4881ef2a57e4a4895ebf52cffca08f8105b936205996a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:23 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:11:23 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:23 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87847ff069746b895df25f88cf86a650c38d1d1bbdfe97b68ec3995ed6c1391b`  
		Last Modified: Tue, 09 Jun 2026 21:11:39 GMT  
		Size: 76.1 MB (76058547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:58f1a3a05c9ac7b752add4a29a9a18803576bce30517a0d3ac70b3bdf19ebb69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d64c46319b0dd251a104e2f5e7aeba6b9694b5fa3b6b8218636a253aeae2b4`

```dockerfile
```

-	Layers:
	-	`sha256:6033439b950150e26dee53d1c21c4419fa7c13cb4c6afa8c5a4a73dcbae1956e`  
		Last Modified: Tue, 09 Jun 2026 21:11:37 GMT  
		Size: 5.2 MB (5203271 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc381e16945d4eabbb65010d76e34a185c76a4aa460fc07aa884b88c9a1bee9b`  
		Last Modified: Tue, 09 Jun 2026 21:11:37 GMT  
		Size: 8.8 KB (8782 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b223a33aee66c870514722c799e95d27441f18724ea7ca55f0bec9bb090a8616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128762625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a655e3c030dc7f9bac0fe70f4092d376e534f849b9b0acd397baa3a246c0e95`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:11:23 GMT
ARG version=11.0.31.11-1
# Tue, 09 Jun 2026 21:11:23 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:11:23 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:11:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49dd1f0eeab7a7f4afbc23256e1c06db130721f9caae41e6695b493d757f42d6`  
		Last Modified: Tue, 09 Jun 2026 21:11:40 GMT  
		Size: 75.3 MB (75304798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7124430258a445a0dbf2b2a73c8d82dd8a5ae721a625f03cdfb0f52677cdd33c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:188ae93311e3ac3a99895f404f7f4d75e60854bd3c39e9cb2aa3d18e4c9c6f63`

```dockerfile
```

-	Layers:
	-	`sha256:ab1e503394641f21378175df5120470476d1bc10d785b2386618d6bb8e6fe231`  
		Last Modified: Tue, 09 Jun 2026 21:11:38 GMT  
		Size: 5.2 MB (5202889 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbed79a970d0efea852d631e7af3d3f11499afb0f1b465d0a1bf30a09f65f7dc`  
		Last Modified: Tue, 09 Jun 2026 21:11:38 GMT  
		Size: 8.9 KB (8863 bytes)  
		MIME: application/vnd.in-toto+json
