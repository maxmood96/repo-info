## `amazoncorretto:22-headless`

```console
$ docker pull amazoncorretto@sha256:5d937a9098b57c15c3b5fc3d32ed224d914a716e57b246d79b81dbe16504fee8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:46b9fca3019b94ea7555ca14783fe1309bffbbf23bce656f2af45540b1849106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140663514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a65d80ea3ccbe5ed5c5c60f6f1d733eb9148fe31baff98ca6479ea416a76e2c8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c56236f9382f1b5938bce45fdb924bbc107ef936df014ce0cbd86d78f266c28`  
		Last Modified: Tue, 08 Oct 2024 00:00:45 GMT  
		Size: 88.3 MB (88338209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e3ebbd6ee811c08122d3b6b05636c6b3099249d51762b97cf736aeb8bc330db5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c05e1fd9946d2ff9de810e98af00472fdf5291dbdc5bc0b66644720a607787`

```dockerfile
```

-	Layers:
	-	`sha256:46ac2dab980dab1964d87d47b8802efa75a863d936f97ed54a3f5d2167e70a63`  
		Last Modified: Tue, 08 Oct 2024 00:00:43 GMT  
		Size: 5.2 MB (5187328 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01fd14f482f13f11f4e184824ad68cdba56549565354aa24965928bc6fa20ea5`  
		Last Modified: Tue, 08 Oct 2024 00:00:43 GMT  
		Size: 9.0 KB (9041 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:25d9c075d2fdbaaa46476ae5e9d4ef620930dbb3c16cd0fbb202893b2a4a66d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.7 MB (138716194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6edec95ab14f652ae44da0b506b7fb331cb71f3692a7ea10bed51e29c59cf1d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=22.0.2.9-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68b3182c2bf4f49b83ffd7963b1f32d7746c8a8cd6c283e4e96e1f641e03de4f`  
		Last Modified: Tue, 24 Sep 2024 02:47:18 GMT  
		Size: 87.3 MB (87290202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0dc6ff0e790aa36309e578014b2625eec1632b63dcf1b9233323d06399b2e88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a011756f71783471d2a51f02bfb3389de0f98b5adadb504a37e808fc64ca50d`

```dockerfile
```

-	Layers:
	-	`sha256:06b9015a23bae471409672eabe86592a1229e9584aed9d718eb91d0ffd532f0f`  
		Last Modified: Tue, 24 Sep 2024 02:47:16 GMT  
		Size: 5.2 MB (5185299 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83c776681d4d6dd74ec4edd2b028acd23cad0e21c49de2c4cfb3ed1186ccafcf`  
		Last Modified: Tue, 24 Sep 2024 02:47:16 GMT  
		Size: 9.4 KB (9411 bytes)  
		MIME: application/vnd.in-toto+json
