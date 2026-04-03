## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4757b63838092ac9d2f823a2f5b8d10b030e9ad11cb59ff8140e9cf9379416e4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a1322c8c0f001c41542bbda5113d880e06554573f4d212e019df15ef6247c1bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157642534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c097fcdd75b4e2128da96c214a0daa855a79a460943928f12fae54d3c12d6e0b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:10:19 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 17:10:19 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:10:19 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:10:19 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:10:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05899c355b428e826c4469343dc5452344168c847301f296be46feef7c29fed`  
		Last Modified: Fri, 03 Apr 2026 17:10:38 GMT  
		Size: 103.6 MB (103609444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:572a146ec50465957fa863a46b21b15cc16b311806358bbf1dfa12db7949ba63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df930230dd978cf16ef5b56646ce90c3c4b19d3152baff6191eba363d99a90f`

```dockerfile
```

-	Layers:
	-	`sha256:e27d5f51a7639df64cc1d589383af7a8c57ce293430cd0937412b381bf654318`  
		Last Modified: Fri, 03 Apr 2026 17:10:35 GMT  
		Size: 5.2 MB (5194861 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d130273c48819feb9386f26cd370a56ee2963fe4575562aed0ef5fc6d7ba4d99`  
		Last Modified: Fri, 03 Apr 2026 17:10:35 GMT  
		Size: 9.2 KB (9200 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:54660ee1370aa25deb600d650b75c19bac575622443677f5b028b4bb5c8a19e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155472275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9175f8d7db2b034541f63c591ca782912b5a794c89d9e28aac1ffbdb1a57e0b5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:18:04 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 17:18:04 GMT
ARG package_version=1
# Fri, 03 Apr 2026 17:18:04 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b987900f01351009373a3351a1a54c264fdd0855a89a4d4f6dc4ecc36b2d37a`  
		Last Modified: Fri, 03 Apr 2026 17:18:24 GMT  
		Size: 102.5 MB (102530900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eeda90b918b0f258263e97e9da38d8202d9b0783908d592a2227b7a4d918071a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7568f6df5c0dfe0b54aa50f1af32b4a146d12544af2e44e9c082320bbe070e09`

```dockerfile
```

-	Layers:
	-	`sha256:253dcb674beab93c71cd97846f275bfc9a6fcd52c594fff49663561093581972`  
		Last Modified: Fri, 03 Apr 2026 17:18:21 GMT  
		Size: 5.2 MB (5193672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b1bfd37702ff93ff5cc9133802bd2d3d62db35d7887478d60cca26e81cd03f7`  
		Last Modified: Fri, 03 Apr 2026 17:18:21 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
