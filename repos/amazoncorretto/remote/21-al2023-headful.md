## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:4ebaabdc5a4badc3045e133a96f7676531903a8208de1810784a45bebf9fb714
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:262d2dc547a0c509627b0a8efaa1fee8664e920f57769702f21b130a9f642d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144664059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ba637a4affe364e916324e1f6771935a3db1c99cdd8814537032ef67b047c20`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:24 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:24 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:41 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:41 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:41 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:41 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:c7345fb8c6516aa8699c6c7bbaf8e24d23986ed1d45e3b67479ea9e82b49eb0f`  
		Last Modified: Wed, 27 May 2026 01:40:55 GMT  
		Size: 54.6 MB (54571156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15cec13500aa831d874f2efe7bc6f86b880b769df9c7a71a705793b632493bc1`  
		Last Modified: Tue, 09 Jun 2026 21:13:00 GMT  
		Size: 90.1 MB (90092903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ed26a08eaae4b13fddfea6a0322f73397c3d483cef8194ac8ee52aafbece7a62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5226273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71221bc8ed10fb80fc30702094676f7301b45c96e000721ccce9c0092462461e`

```dockerfile
```

-	Layers:
	-	`sha256:ba4cb0f93a2fc348b2ab9414cc22256720ed811c84a9933c2ae4a00c7bd20fcd`  
		Last Modified: Tue, 09 Jun 2026 21:12:58 GMT  
		Size: 5.2 MB (5217220 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af3a5d273b3a813cc2b0d2c069946009ee71a9eb0929406679d32f510d7ab588`  
		Last Modified: Tue, 09 Jun 2026 21:12:57 GMT  
		Size: 9.1 KB (9053 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:53e1e75d536364f058ed53823c140f63bb17e26dbb4f0170e7231a72625fdd2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.7 MB (142688171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26f407472a8431e03cb4a10ce81da41c7c0ea22c6715fa96b948ea96a34ef433`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:21 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:21 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:29 GMT
ARG version=21.0.11.10-1
# Tue, 09 Jun 2026 21:12:29 GMT
ARG package_version=1
# Tue, 09 Jun 2026 21:12:29 GMT
# ARGS: version=21.0.11.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 09 Jun 2026 21:12:29 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:be978697b103a5510665f41ccd5a573d7d49b6e7bc9cb397e03f3d1d8f0345dd`  
		Last Modified: Wed, 27 May 2026 01:58:57 GMT  
		Size: 53.5 MB (53457827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccf742cf29aa9db0ba930644edbcf3894b9e2c16f115605fe7d45d3f038f5f4`  
		Last Modified: Tue, 09 Jun 2026 21:12:48 GMT  
		Size: 89.2 MB (89230344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:19292e93a75e447de55e2452ae0300ac820e6406731f825d0a67ad6a315c408e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f31561f698c929384fb0791e0e2f70ca351709acbdd6580d8aec9e52a1b3f6e`

```dockerfile
```

-	Layers:
	-	`sha256:7da0ef600fbdc1c1a1187ba9658879016377565861622d98942867a31c13d58c`  
		Last Modified: Tue, 09 Jun 2026 21:12:45 GMT  
		Size: 5.2 MB (5216014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fec6742bedf18eef656aa0f3216160fa45da5a0d06c9ab7db3c2795f7cb50689`  
		Last Modified: Tue, 09 Jun 2026 21:12:45 GMT  
		Size: 9.1 KB (9133 bytes)  
		MIME: application/vnd.in-toto+json
