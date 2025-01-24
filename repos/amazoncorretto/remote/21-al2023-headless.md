## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:0d3f923ead1f6568acba1fca9957034c45c992e12e9508052ab674464bbf6004
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4fdd17b8a8b1a98182500fe97a0d0a678532a624394ac0f277c8ee05ecc531ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142114942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a881c3d3f2db759a4c4af60d4033de10245b722ba98523945fa025d822f13dfe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:40 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:fa97b7596fdd91f8ccf1ccf8ee7189f9449877cc795e39ad814638444b666c80`  
		Last Modified: Fri, 17 Jan 2025 02:00:45 GMT  
		Size: 53.2 MB (53152535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d062d4afdfe32318c4e5cf71b5568026f9e72569c5e9d79d8748836c137f9dd2`  
		Last Modified: Thu, 23 Jan 2025 23:08:14 GMT  
		Size: 89.0 MB (88962407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e6d44ed298bede6dfb35fee438432e61fa903cacbd693da71c7b8fed89cfaead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:672141183cbce5e2785bd66d4894d4a5d08edb1e44cbaa659cdfebcff8bf55e8`

```dockerfile
```

-	Layers:
	-	`sha256:ff3cd4e5a94ce07c187ceeb2557aa28fcf433b019536cb994b6cbc1ec271f053`  
		Last Modified: Thu, 23 Jan 2025 23:08:13 GMT  
		Size: 5.2 MB (5181038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:931bcd8c21d64ed64e7936b3464a0eefab6abcb9b86a6d11cf92a9eedb7e77b9`  
		Last Modified: Thu, 23 Jan 2025 23:08:13 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1b3f238b9618e802858b909f9b8bccee4ae62451dc9b552c6b21a593ddcff91e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140370803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5df6d4bd48d512a4422c433ca09929acdcb357150ee82876a481d783908ffd0`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 00:42:44 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 00:42:44 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:23c58bc83b4b2c70780808282eab12c25cdbe212cc6fa4cd0d9a4d82b1cbf7ce`  
		Last Modified: Fri, 17 Jan 2025 02:10:39 GMT  
		Size: 52.3 MB (52270199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49adb75ab6bfcced36240a533734176ceae65f28dd7dfc42116e829185124667`  
		Last Modified: Thu, 23 Jan 2025 23:24:23 GMT  
		Size: 88.1 MB (88100604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:71c7021ab3da3e8c98473f82ce329aec0c5bad6de0ffd1cbfe042c032111c432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50b1c04fa708d2494b2d9d321d49f8aa60a7bcb8c155c5077be0cc6fb1a5c9d9`

```dockerfile
```

-	Layers:
	-	`sha256:713e342e6762968240e8eb890675b1dbe39614b5857b83b42933c1bc600feb9d`  
		Last Modified: Thu, 23 Jan 2025 23:24:20 GMT  
		Size: 5.2 MB (5179828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14174a006dca735eb553eb1aa1f8ab5bee48542bc459dabd572d1923fb8d376c`  
		Last Modified: Thu, 23 Jan 2025 23:24:20 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
