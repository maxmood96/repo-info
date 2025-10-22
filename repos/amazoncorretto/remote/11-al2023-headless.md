## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:0f3097c1cb51e9a175743ecfa30c74a8b2bb0806c81cba5706a665df0aee860f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:226eea13809937d6e5db24692ebc8c0fa96567bd24cf87fcf3d8e24af9ae5af9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130020556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:429c3c664095469118acdca9642b2d2a851f5ca37fdfab75598e08fb220bc983`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:56 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:56 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bec9e9ab9445d6f89b267a81c3680402542b5995fa3d4293d15be28c24a9bb30`  
		Last Modified: Tue, 21 Oct 2025 23:26:58 GMT  
		Size: 76.0 MB (76015425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c666a3bd428dda4b9a88735a4d7dbce35177ccff6554341019c38cc7866ea886
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241f95cfa6538b2ce03d501a5f6180030f52303b40d06a2a4e365557a49d07dd`

```dockerfile
```

-	Layers:
	-	`sha256:afe3f0b6d99bd3da3302adea806a0bb44d7ee10eacbbd245a6c7cee03245f1cc`  
		Last Modified: Wed, 22 Oct 2025 00:47:58 GMT  
		Size: 5.2 MB (5196743 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4bd903ece299bb78c74f78805eaa2c6faef8f171dba52d8e5b67687297b4925`  
		Last Modified: Wed, 22 Oct 2025 00:47:58 GMT  
		Size: 8.7 KB (8652 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c417883cfbac662ef2114d264ea6212e9535efa8dc542e8c2af5f5a86013aec7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128134678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609abcc363be00277cd123b7b440387144a10ec7577d642683375256556f475c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 01 Oct 2025 20:24:59 GMT
COPY /rootfs/ / # buildkit
# Wed, 01 Oct 2025 20:24:59 GMT
CMD ["/bin/bash"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=11.0.29.7-1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d2b80f9615d7bfd0fd6e732a3084c8d2522dbf847ef50e5d7f314366130ba8`  
		Last Modified: Tue, 21 Oct 2025 21:50:05 GMT  
		Size: 75.2 MB (75243475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e546f3848e1e43c17dfc932d99daf867b0a2047765b90b900cb8fe1d4288ace9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb47182379a4e3651e50e86fd7f2db9dfabb4932244112a06dc4e8141a67e34`

```dockerfile
```

-	Layers:
	-	`sha256:d5cefd0311d5ae80c4c6d27d4e937ab5e1d58b2359d0b6b1018380caf58d4c5f`  
		Last Modified: Wed, 22 Oct 2025 00:48:04 GMT  
		Size: 5.2 MB (5196361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf7c3b5ea60b0bd5d6e5263f34e2ca8e696a78051961dc6d35eb7d91c569dc12`  
		Last Modified: Wed, 22 Oct 2025 00:48:04 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
