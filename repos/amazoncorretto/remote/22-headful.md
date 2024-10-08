## `amazoncorretto:22-headful`

```console
$ docker pull amazoncorretto@sha256:17d195e1229427aed2ac294510f1e9e4c33117a3f0e6b3ac5a767e4f1135c3c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2a31dbdc8e8a89d86ca8d3e4494519bad510313a61d961d381ffa350a4b18eda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141367929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:739a3e72bb97444f209cf6f880d3b6fdd0409529538d86c3fd0e8f8f593d699e`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:9daf8e9a9fdf6d601d62aaecbd7b1d0e51a18b697c0e7e68968d02bbd66a34ea`  
		Last Modified: Tue, 08 Oct 2024 00:01:09 GMT  
		Size: 89.0 MB (89042624 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e1ba5e7b766f1654e392f5d3bf5513a1fa7c6f21fcd0e8715f971fd81f08409
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48fd505c1ebf6d646e8271f7f5e145fffd976ddfe6ccb4a8901a55d81215ac0`

```dockerfile
```

-	Layers:
	-	`sha256:fea84814fcc65107a57d2fa5fbc32038bcc6960ba2575339154d80c8942f2239`  
		Last Modified: Tue, 08 Oct 2024 00:01:05 GMT  
		Size: 5.2 MB (5212441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9f8e022908b9f4e1f2a893c13a8f6313aaa0ffbab5a826ee1eacb05a2b4558e`  
		Last Modified: Tue, 08 Oct 2024 00:01:05 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:db9b66990374e48ae21b0a3a70a7c7f5b8c13d5401b16fbd0c90943c297d1734
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139434374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd581bb9d25336d644bed6b4f408c34bb2a4b7223de3dadf6ca8df5175831e45`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:697d04f623c6880c377f4e1515950278fa3e3e29e0e6f3639ec94a607a52eee1`  
		Last Modified: Tue, 24 Sep 2024 02:48:08 GMT  
		Size: 88.0 MB (88008382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c4b52dce7bb80d5074c095dc93c1df28b99f4f93cab7cbcac3d36cc4afc7eb4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2459603f8ba3db97001cc673bc13c32bf5c228232b6122ebf83b1b1f11d72da0`

```dockerfile
```

-	Layers:
	-	`sha256:892e092b9caad208ddb870507e590d6d8301d4bcb073bbb285b09b5ef66ef792`  
		Last Modified: Tue, 24 Sep 2024 02:48:06 GMT  
		Size: 5.2 MB (5210415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b003718227aaeb8180289066920d75333bfcebed1d04d21db395c5c8f84c812`  
		Last Modified: Tue, 24 Sep 2024 02:48:05 GMT  
		Size: 9.6 KB (9588 bytes)  
		MIME: application/vnd.in-toto+json
