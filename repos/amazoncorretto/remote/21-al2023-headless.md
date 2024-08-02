## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5ed724d58954447a7952b6743eee532989729d858b7f57cefa8d20cd9515e838
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
$ docker pull amazoncorretto@sha256:dae236934d77e46948525c27cad50f1ade59df70cdcaab19a5cef446f61868c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140028083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6600b37db71c462ff18d01131ba81f2b4d33b3bc068e618d47b1e49b46ba77`
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
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32156763bbbf2a7fdf3b06cf7c795e7c33ede46d8dc51823a91fca275d8b2d5c`  
		Last Modified: Fri, 02 Aug 2024 05:49:30 GMT  
		Size: 88.6 MB (88626071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc1d52550ccffdb4c39e47fd8b9fb176d8fb7f719dd13abd1a563f8edf5068d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98413fa5872ef2925f6320d4e8744af16a16e47fa208e5ccfbd449f3bb0db21e`

```dockerfile
```

-	Layers:
	-	`sha256:da22e2e24da4e43eb7a32562b54b6d0a284c3b7add4a9cc9f8755c181ba489fb`  
		Last Modified: Fri, 02 Aug 2024 05:49:28 GMT  
		Size: 5.2 MB (5184829 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36a63ee970b272a95a313dd4fa3b3448308e9579245cd55caa4bf01b77df2f8`  
		Last Modified: Fri, 02 Aug 2024 05:49:28 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.in-toto+json
