## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:de26239c67b9804032f7e809cdd0ef0db69ff74d69f1055766a6cd6a9fcdedda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:eca16c8b25fe63d122b1fcfbe22dd49eb2d587de6b1bfb1ee28ff8e9763e06e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142131559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad40aa021cdc5a62326a6eb0364cf81788cbb24c1be957008c05d2437ddec30d`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:7a00533049ac1103519dcf69bfbf117dc8fc749fd2ac85a1940fdb4db4df5d39`  
		Last Modified: Thu, 27 Feb 2025 21:08:29 GMT  
		Size: 89.0 MB (88979826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b88820f814111b2dd1504beb03aec9a658c9bd1d6200d71f873e5517de1a721e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5b5af2d20dca4a346da4412f181abab933f9cbe687d98869cc4ebb0924dfcb2`

```dockerfile
```

-	Layers:
	-	`sha256:c224b0c1e9c1b5b3181e147459fe003ec7ba175645a696490cc946d49d567d9f`  
		Last Modified: Thu, 27 Feb 2025 21:08:27 GMT  
		Size: 5.2 MB (5161330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d752ebefb82866346a59814becadaabf28e1cf495f823fd737a9ae943fa2f38`  
		Last Modified: Thu, 27 Feb 2025 21:08:26 GMT  
		Size: 8.7 KB (8747 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:80d9fb74239928b575a4a58a6564d0bc7d8e834167d8f8da1c0bc4ebfcdc593b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140384192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8eea52452a16dfaa07d3b79348309b4d5c2c7241167c6a77c0bc4dcc865732`
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
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
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
	-	`sha256:123333a6c7628db66abb1f64986c0e89fa4478abad14b5e5bb9492bcdef26acb`  
		Last Modified: Thu, 27 Feb 2025 21:23:15 GMT  
		Size: 88.1 MB (88112922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a01b596103417567fcdfb8a1f7b05294a95ccf67836c91805495809ff210ea8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275d94256132b6a3886aa0f6321655deb21da2c502a75a67aa4c433e5d37c13f`

```dockerfile
```

-	Layers:
	-	`sha256:75eb47f8d6e5adb2dc2d77cd86f94055332565232ede7c270c9edaafccf2131f`  
		Last Modified: Thu, 27 Feb 2025 21:23:13 GMT  
		Size: 5.2 MB (5160120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4211bd28797d9a20906f029747aa68f92eab896dd19f0b879409012d143dcd69`  
		Last Modified: Thu, 27 Feb 2025 21:23:13 GMT  
		Size: 8.8 KB (8827 bytes)  
		MIME: application/vnd.in-toto+json
