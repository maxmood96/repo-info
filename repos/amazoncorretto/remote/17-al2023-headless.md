## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:0ca91af874b151c9ce4de662f440c13d849444841033e6bfabfe8aab6f8914ff
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fe29a5a7f2603cbe262f74daf396dd409ee19092ec0d7049972bb677f8d631aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135283996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ac42d00f1b495d887b52ba8159230e8a0a2d3199fd443e919ec8d83b58ed1f8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0b097f308b6a69a495d5e5a13cf9ca5207eb7ed64da7124ffbd0d34037edf9bf`  
		Last Modified: Sat, 22 Feb 2025 01:44:44 GMT  
		Size: 53.2 MB (53151733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e788bbacdc271d29291e9c4922770d0f411ee4c0a85d90b1789aa7d6274c9fb0`  
		Last Modified: Thu, 27 Feb 2025 21:08:21 GMT  
		Size: 82.1 MB (82132263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8e4f5baa15b6b01043d9abf1efc5c9df9225c90b21b0dc4d9532684748af77e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b194bbb180382b861c94441156e0b38ddc1cc9bcb030526a62c37c0275bfc62`

```dockerfile
```

-	Layers:
	-	`sha256:10080521a2eb5325b41ba803ed0121308e7b45f71509cfecb9ce2bcc14fee107`  
		Last Modified: Thu, 27 Feb 2025 21:08:20 GMT  
		Size: 5.2 MB (5159712 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2aa76906c7d33e88c6b9033a3f257839d78502fc717cce593c148a8774084b6`  
		Last Modified: Thu, 27 Feb 2025 21:08:20 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d4ddac51f13af63c7696ee108c47e1feb735f0efb4870b17be3fe28409e978f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133822547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02da25d749151c3f12aa192b5c8e15bc8cfc8299e19e089761432a0a9ad759c6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
ARG package_version=1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9f14bc8b911d112fe9005a1fab86d88bf14a10f429f49d6291fd5e2395fd4442`  
		Last Modified: Thu, 06 Feb 2025 18:59:08 GMT  
		Size: 52.3 MB (52270951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9401aa851ae176cb396b61d9ba3db43844a1ce1ea62cedfd683a8fec299fb0c4`  
		Last Modified: Mon, 10 Feb 2025 20:21:52 GMT  
		Size: 81.6 MB (81551596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6239096e5ff86879b48ee57a7c4104a483ac6e84fb2300f1bd8bd76e4b533a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5167331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f08d4472d7990127358831c055cf49519b9eb1b00db609f183c9a7af0888af3`

```dockerfile
```

-	Layers:
	-	`sha256:58a0c892c98ea9dc53d87607772cbbaa304a63404cb07a0859539cef2d19c665`  
		Last Modified: Mon, 10 Feb 2025 20:21:50 GMT  
		Size: 5.2 MB (5158500 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f106ecb24a9f0116cb9fe85c9a3ae0896e76f428b3287eba8fd78f71a8eba6a8`  
		Last Modified: Mon, 10 Feb 2025 20:21:49 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
