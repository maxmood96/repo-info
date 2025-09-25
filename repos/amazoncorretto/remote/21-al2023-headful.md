## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:4227afa49ae4d74d5dc3912e50b4c095fdc31d24c20a7c6840ab3bd0762fd8a5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:82e2ef0fff1202c87b7da54ad0441c20b597053c22503ffaf91d67e4b004981a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143971662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24bf6324d174b7f3745014619cc653fadc5465802021a4d6a1fb1c8dd7ffabe2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a2e973bf5ed8da4d9b082faf2f33554edbf3d94d2f98208993c4d19b86ed415`  
		Last Modified: Thu, 25 Sep 2025 02:16:29 GMT  
		Size: 90.0 MB (89966382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:357c259358b67554816e213a924cd7faef3e8e6aa4b51c804487a101000a4d91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b18674608814e2633b909f3da5e8c52abd81e14471af54c868a8f9071d37b3c2`

```dockerfile
```

-	Layers:
	-	`sha256:8f34565b92599d036758c05466a00ba0ae965f7abcd5ef2a0d0cef28c7d89d0c`  
		Last Modified: Thu, 25 Sep 2025 03:50:21 GMT  
		Size: 5.2 MB (5209861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da697f353bf8c5888fd0a8742749121bc32810b153f611bb3ecfd8109292cb07`  
		Last Modified: Thu, 25 Sep 2025 03:50:22 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d52b91710ef01019a000017c20c3a81db7367627fadc4465cfa1ca54040b6bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142000205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ee40c4d5b893fae0906d0dc0285045eb19b11ed409be31ec2dcc3663e4a482`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbd27153e15faa03759ea9641544ddb9a7538f9dd9f1493436110de5875f8441`  
		Last Modified: Wed, 24 Sep 2025 21:14:08 GMT  
		Size: 89.1 MB (89100767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:40bc60ff2217293e1c14cb0f63fde9c4320aacc2d477bee867657568ffdf134f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035e6c7804dc6627622cd468cc4c3d8750943fcc284690a85263bbbd3494b2db`

```dockerfile
```

-	Layers:
	-	`sha256:5dd4122a55f804e5616f9cb4ed182e3f492417ca422ba1c4a492b9f63edc6b2b`  
		Last Modified: Thu, 25 Sep 2025 03:50:27 GMT  
		Size: 5.2 MB (5208654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:954044e68a7c5cc131efafec199f60d8174958975aadcca221915843297b501d`  
		Last Modified: Thu, 25 Sep 2025 03:50:27 GMT  
		Size: 9.0 KB (9007 bytes)  
		MIME: application/vnd.in-toto+json
