## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:7604fba0314a4b1b05ebc25f95fcf84be56a6143b67202a346ecf187d289f14c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a990631ad79887b9013444b39a91c665220e5768b4fbfb9559bfa72465c94c56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.8 MB (143823234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fe7aefa2dbb672e2b98fc796b88b02d48aedcad6d00a32c95bf735a56e61ddc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:989d4a8a2accd45b05933473a235ea401b52185c3db1c1bf8d953380af6a7341`  
		Last Modified: Mon, 18 Aug 2025 22:37:34 GMT  
		Size: 53.9 MB (53868730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c668a4b3148472d6a7e12931d562eed3004ef151f6aa1c027f56044aa756ed9`  
		Last Modified: Tue, 26 Aug 2025 00:01:15 GMT  
		Size: 90.0 MB (89954504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:78bce477a4e34b5caf3a2c83be9bc014d38453f2c11579daa725231ccfd7f26e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead8bbfe20440a1a6a90b2443ca6efe61b14b28d387089bb9d07bb4c5f93cfbe`

```dockerfile
```

-	Layers:
	-	`sha256:a0551e55feee13bd5029660bb34dfcc234c959461b02e8dae512966239dc3dad`  
		Last Modified: Mon, 25 Aug 2025 21:49:00 GMT  
		Size: 5.2 MB (5209861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da96a5266ceb6ed5919cf1109e0e4aaedc13fac2a6e9a5f7b6edcc932b430d8c`  
		Last Modified: Mon, 25 Aug 2025 21:49:01 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5e2b86bed7ea253e246ea7faeaa6166488fafaed46494129e9a01901658e0d24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141859719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f918795101b1dcaf3c60241c3f266d0cb579a7f6b69fe611dd40cfa9ba2a4f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 18 Jul 2025 19:06:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
CMD ["/bin/bash"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9-1
# Fri, 18 Jul 2025 19:06:54 GMT
ARG package_version=1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f0b7d54214a6f9c2c7698f71fb06f2128097c3f9d97269e3d449f7639c142381`  
		Last Modified: Tue, 19 Aug 2025 02:47:54 GMT  
		Size: 52.8 MB (52768497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f7f2745e70256b3801468348039e779160428c4d677c7a7ab4348728cc6e47a`  
		Last Modified: Mon, 25 Aug 2025 22:25:04 GMT  
		Size: 89.1 MB (89091222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0deff5d510f9555e6c25765b3276b83aa04ce3cd83884e8273de7d168dbf95ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc10272213b5814fc9335b634772587849ee8977c6b893846a7c6050cf1a4890`

```dockerfile
```

-	Layers:
	-	`sha256:ccde1cd75c8425dc802f03484d475727d20dfd2ff836a19843d80d0679ad341c`  
		Last Modified: Tue, 26 Aug 2025 00:49:01 GMT  
		Size: 5.2 MB (5208654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5dab53b9a8a5487c8f0e50a33ea6384a2ac73baf0ab73671e622020ca4ece58`  
		Last Modified: Tue, 26 Aug 2025 00:49:02 GMT  
		Size: 9.0 KB (9006 bytes)  
		MIME: application/vnd.in-toto+json
