## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ac39aadb1eb7e8636eccd92114e4c79ed901e734a1b42aafd55e860db6c10f52
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9cedab15125de5c0104fc9ec6d64601d9c045e5994cd56d01da51ec7096fa5e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.8 MB (142826616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890184903e1a84f1d8d570b2e60bf279af573a9d05fae21890900827fa793acb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f0da59e477f67ee64fabfdbab928ff9cfc86b8b9dd11ba51eff3492ff9ba741`  
		Last Modified: Sat, 11 Jan 2025 02:29:29 GMT  
		Size: 89.7 MB (89676141 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8d58ca69c6c5bc4c02a39a2dfa13d8e9e72a5984c875aa5d06ca7d25f027bc8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5215224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b6ffaf879784eec8c19fb1aab3d80ec4266d2974293146d6503952d8f858dc`

```dockerfile
```

-	Layers:
	-	`sha256:df32a3f541eb78cb3da3fbbdf1a0236637a5c4ed54df540128ec6126e82b78a0`  
		Last Modified: Sat, 11 Jan 2025 02:29:28 GMT  
		Size: 5.2 MB (5206292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94972dd4c6ae312a3a7e4679a5b25c448e04a203e861e878a4905d0a55f53bb2`  
		Last Modified: Sat, 11 Jan 2025 02:29:28 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0379daa534b7e7d2057d2643af17b97530ff35527f45867d21468b096345c3af
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141102363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678e8fb9320af1d71105c799040b70ddca163f9b7a7bf420a01502ffbc731c82`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2261e8979a37564ced0e0ad9a5e2b9c93637eb2abb64fe26e57cdab954b37bca`  
		Last Modified: Thu, 23 Jan 2025 18:52:22 GMT  
		Size: 88.8 MB (88834167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb7d3ec7ccdc40c82a9473dc8ffd2e4c79c5a4f5273dfe97edcb8ecd34d353fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5790d32e828d36d05258ac14750b7d06baf9a47bb2c5c96207eb4c86e7451a`

```dockerfile
```

-	Layers:
	-	`sha256:0fa184cfe512180d087ed3e231fa1465f6c0f9190b0bfcc7f4de663d27c22ad5`  
		Last Modified: Thu, 23 Jan 2025 18:52:20 GMT  
		Size: 5.2 MB (5205079 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3360288f844f5de07062826cedd86de583a1df16d3032d51211b56e8f8745960`  
		Last Modified: Thu, 23 Jan 2025 18:52:19 GMT  
		Size: 9.0 KB (9006 bytes)  
		MIME: application/vnd.in-toto+json
