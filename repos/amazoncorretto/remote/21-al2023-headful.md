## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:51bbad626bc0359955981e9b739998107a3c65f8c182dfeeb70b98f4e62fb20c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d3bee7744d5d2304ddbab1203ed2bf5bcb68baf0fa09223732a0c2b6d9ad3712
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.9 MB (142856268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff0314577c0f33a1c98a00325214faed149f826fa2bf443c9e56d9df06fab01`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3cd03c52a10e7531f607c84e6815384cabebe7188ead38697fcda8775c7134a`  
		Last Modified: Thu, 27 Feb 2025 21:08:22 GMT  
		Size: 89.7 MB (89704535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47cf6ed3c3c9a4059a86a296c4ea9cbc5c71570499c0925837d36c4e98b930c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5195505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745d423fe4a7d2be8760016243f83b61621298c1f705f3aa32efa51f250e8879`

```dockerfile
```

-	Layers:
	-	`sha256:2eae07a6f40da44b0f2883df4f18798d0bfae49485b19b806a4b9af5ea239e7a`  
		Last Modified: Thu, 27 Feb 2025 21:08:21 GMT  
		Size: 5.2 MB (5186578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bca4cb3fc48d5cdf8a3e7169ba046c6fca7609bc66be07903b7d838f917887b4`  
		Last Modified: Thu, 27 Feb 2025 21:08:21 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:34801a748c56794fb843300fc8990ade3ed756abbcc9bb8de5806da613936cf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.1 MB (141118124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:314fa626c633d9c81b054f152e179bc5c5efa287b40ca110bf94394f96c9e438`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ae97a46dbe642672a09bd4ab6df7280b70a40f641ef4a637aa82879145ebcb67`  
		Last Modified: Sat, 22 Feb 2025 01:44:42 GMT  
		Size: 52.3 MB (52271270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75d02eb953541c2ff90ee6823eed21e190b64fc35f6038a407ba5cfed5ac783`  
		Last Modified: Thu, 27 Feb 2025 21:24:00 GMT  
		Size: 88.8 MB (88846854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba9dd54492c31d5511b96bdcde1ea24a26ee3a90e9d72008c8d3b86821077ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18e8768fb283b2136b8065d7f2d263ab7723e734ab13a673e36225a15d5f8776`

```dockerfile
```

-	Layers:
	-	`sha256:56c4c68a2ac90c8ad2b3b17e4f0c89af38edf53d2faeff4c44fd6bd69ad96e72`  
		Last Modified: Thu, 27 Feb 2025 21:23:57 GMT  
		Size: 5.2 MB (5185371 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a3472448c49acd0b59923e2381b1c99f7f27e0f2dac020ddabac153f4ae0e4`  
		Last Modified: Thu, 27 Feb 2025 21:23:57 GMT  
		Size: 9.0 KB (9005 bytes)  
		MIME: application/vnd.in-toto+json
