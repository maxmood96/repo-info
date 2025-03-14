## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:3c0c38ee098477cde15893ef08874b37d4e8d843ab555e185014dff7d31004e6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bb49bc873bba2789caa93abc3157f6f25f6ae89e99b696f8dbbee87c0119a9d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142105587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46596a8b5db263c51b0bf6a6c2c75182c6def2c5827c70264b26c549d74c2ad`
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
	-	`sha256:9ec3516d0f4b07a63d66d796b21f72a416a1968c512c2a8214a11acbb4bf7d0e`  
		Last Modified: Fri, 07 Mar 2025 22:16:15 GMT  
		Size: 53.1 MB (53126876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88d5eae647b4d0474acc1794ce2b3e1a0422f6b99b3b7e6c838092321137b4e5`  
		Last Modified: Thu, 13 Mar 2025 22:53:05 GMT  
		Size: 89.0 MB (88978711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8e1dbfb309185b37280f17ef74ca40b3fd055030b3db2b4903ae20c24c3a1b81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48bdee01d657cb6c6803c13ad25c2a6a49e4730d55d22fa8d4fcee88f3f8553e`

```dockerfile
```

-	Layers:
	-	`sha256:7534528829722b4bcabc890b8609cfb4a53f8bf6aecf74151ef53f91550b01b3`  
		Last Modified: Thu, 13 Mar 2025 22:53:04 GMT  
		Size: 5.2 MB (5161330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52c467994f3414f77258c6d4b0d1f186443fe6e07e66c9ac8530143f10065416`  
		Last Modified: Thu, 13 Mar 2025 22:53:04 GMT  
		Size: 8.7 KB (8748 bytes)  
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
