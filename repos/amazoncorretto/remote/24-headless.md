## `amazoncorretto:24-headless`

```console
$ docker pull amazoncorretto@sha256:1cfcca592e70cdbeafdb9c69b57d3d99d4449cec61b24d4c9792e60fec33305f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f24bf5c0771123db51aa8d74e2cf9947d3f221bf03e3d86ed876e9ffd99786bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158259674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d31e223a273a48c0a6ac02e5f5969bde0966f28b070ebc4c1f80295a3eda4311`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5206867b09e6decbf1daa0ecad21b77fcc0ef5192543451a88c3765fc787e8`  
		Last Modified: Tue, 15 Apr 2025 23:56:11 GMT  
		Size: 102.4 MB (102352621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5d7eda9811993cff6eea1492a8b8be70069d3373cbc335dc4e655067e3ff08b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5446730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4168aacfe48ac48a623b17fdb439805e3e6e31facffcd1dfd4ef563fe70c5f8b`

```dockerfile
```

-	Layers:
	-	`sha256:18acbfe76de872b62b22e92489a33e56920d0339b661cd96ffdca9764c12d1b1`  
		Last Modified: Tue, 15 Apr 2025 23:56:09 GMT  
		Size: 5.4 MB (5437657 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b5fb0305c19d2d0088cc213943c8fdb0cb38c9edc8043c6ac8da6f472b300041`  
		Last Modified: Tue, 15 Apr 2025 23:56:09 GMT  
		Size: 9.1 KB (9073 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8a65940383abafd98384905e04543c6a937149a65a4e0d615129b44cc1c80c57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.3 MB (156321474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:118b73fc78741614c10da17d70fb7335fab6a18abc45b9c49c2be19eb8f8c57f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a72574e7082842d498c25944fa12504a65536105183ab3cf28544665bc8b7ab0`  
		Last Modified: Wed, 02 Apr 2025 00:39:03 GMT  
		Size: 101.4 MB (101360465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7e20838fb3ad2b069640804e88032effa5d28d038b805d0686688e0b2b593d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba78716ed0f0a833188ff92079a7b1055aab3abf875fc58e1408e9c813fa6852`

```dockerfile
```

-	Layers:
	-	`sha256:55012397522ad60ce44bdc5ea9655477dba7e9966710a935097ed88aa6d9a538`  
		Last Modified: Wed, 02 Apr 2025 00:39:01 GMT  
		Size: 5.4 MB (5436464 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8d3c9ed301c78fd780006ca89a8e05e1cd5e10172a18eff329c97f8aa41d778`  
		Last Modified: Wed, 02 Apr 2025 00:39:00 GMT  
		Size: 9.2 KB (9165 bytes)  
		MIME: application/vnd.in-toto+json
