## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:baaa0f2cc2d4409697842d8918b9e20ae035cbe7a7c645af5cf5a963ddec0858
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7870293adf85294835a389058b71dbe4699b38dbe6655467303c574661b606db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130012873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c387ef1a9206520053c9ee07b364cfbb869b3be3e2fd5c24847560fc604ac6c7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:11:42 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:11:42 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:11:42 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:11:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b60f234b8c901d31cbe4ef77eeffdd0a815f88da849193378de52edaff1b2d`  
		Last Modified: Fri, 31 Oct 2025 00:12:11 GMT  
		Size: 76.0 MB (76011638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a7e80d7ce2ae71e94b8b9a3b47dd7011def6629a4763203051800109d377611
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045643f748d525639e645b4830d57c76263135478994422a01d8fd630025a87f`

```dockerfile
```

-	Layers:
	-	`sha256:20499fa2a49e0549ac3559092041939b77c474498ea5868597cf4d2e7681c27e`  
		Last Modified: Fri, 31 Oct 2025 03:47:59 GMT  
		Size: 5.2 MB (5196819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d38d6db2e8068d40ddf92f14d09863fd77594ee7c439e2cc474f3a80d4faa3`  
		Last Modified: Fri, 31 Oct 2025 03:48:00 GMT  
		Size: 8.6 KB (8607 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:242502103e758d372fc6b3b7283c67f64f246bb2b58846b4ccc2d5ce9fd98127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.1 MB (128143269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ad9e34d7f2c8f098d843f6dac78152a86c37eac526af202aa8512b14eeb4b25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:06 GMT
ARG version=11.0.29.7-1
# Fri, 31 Oct 2025 00:12:06 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:06 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73fe75c1fe8404df301c28a0f8bf740dca26718b9af27f46a3e2cf3e04eb2385`  
		Last Modified: Fri, 31 Oct 2025 00:12:42 GMT  
		Size: 75.2 MB (75241418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8de43aaa193002a174ce9894503006f699968a08a678a88fbd9f788daf38cc0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefc761b054f53740ab4986e0c62ec6f9a32af1eb26916dc9964c99ee9d84ba0`

```dockerfile
```

-	Layers:
	-	`sha256:16e4a66ebd834d7e51b50d4c09136816b5fbd4a1008ca10cdca0a59c3437e386`  
		Last Modified: Fri, 31 Oct 2025 03:48:05 GMT  
		Size: 5.2 MB (5196437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01119358a080d9233c414e5fef3c33bf094db48861eb96d8c5e6a5b2b5b64437`  
		Last Modified: Fri, 31 Oct 2025 03:48:06 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
