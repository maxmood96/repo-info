## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:83ec93ba7346c1ebd33783c2e574b34ea28f2607bfa7c173356ce5abe5a664dd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:032273694aa2395cf04781a8a120fc421d131cbe9c9bbf1cc4bf2f25d6e7dd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142104564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead02c35bdcb8f655afb36690b265ba841abb012578413e11275d7da59848083`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Tue, 14 Jan 2025 20:33:09 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f6f3321126c30e5e5901f85529be69459ee79e3876fe4926cbf121ba800f7`  
		Last Modified: Tue, 14 Jan 2025 20:34:56 GMT  
		Size: 89.0 MB (88954089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8fb5d0c07980b72cbe1b03852cc4c41b02c9f55e01f3102bd5e2a26e38b6b59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a92f314ca4ff8ee4db5791ba26dca5c3ac7c1c5f300a16cff06264b2dd538`

```dockerfile
```

-	Layers:
	-	`sha256:f2a7e2e2ea2656874c4d4212dd2b9ccc3f471d127ba930fdc2f76ff8171948c8`  
		Last Modified: Sat, 11 Jan 2025 02:29:38 GMT  
		Size: 5.2 MB (5181042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a319d7e6faec2e91898cea25675739d012378df7c9e3111c6584ff46992e6115`  
		Last Modified: Sat, 11 Jan 2025 02:29:37 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:63b07cb2739446d2fd12019188e3199fae63e9a23c9e1f2ccebf9405b160c5b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140330103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49ea41c08f2ca8b7e3b59e7ecf67dc0c9670042b911e4a25834696db5ea6e1de`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Tue, 14 Jan 2025 20:39:04 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57a880051c9aa766440c8bbe4a8636ba5e51dc1a892fa4fce0816139743fb11a`  
		Last Modified: Tue, 14 Jan 2025 21:16:19 GMT  
		Size: 88.1 MB (88061907 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:540a96cad9691a8263fec80c957472a8e490c1929152ec6cdc18ab2f98471cd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d7264e605d920e75452a0008912a3d7de1a9865e20e2a2190cc723f4eac414`

```dockerfile
```

-	Layers:
	-	`sha256:ec2372ee6ee2255732dff5a8c4ca271e5b13341251b46756b01323ebcb3966c0`  
		Last Modified: Sat, 11 Jan 2025 03:11:04 GMT  
		Size: 5.2 MB (5179832 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18a12ea554aeff0b9397093dd020f53267294b4db862673c829c1acb2e076f6`  
		Last Modified: Sat, 11 Jan 2025 03:11:03 GMT  
		Size: 8.8 KB (8829 bytes)  
		MIME: application/vnd.in-toto+json
