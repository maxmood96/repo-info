## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:4a1a8052a6cb9c56ba22614cdfda4857f4f7cc28796e53aba97a716f751613f1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16fbbdb6c799218e75cc0ec509833885abe052f6e2f3c75fbfab59deaff24dd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134414049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20494ae4d25abbd8cf13732ef8c2f6a51ff179d2a695a2527d9f27e39611f0d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5f3b500dc43eba4cfdf8e70913f712bd20874deac837800a822eb046b9b8bd01`  
		Last Modified: Wed, 06 Nov 2024 19:16:29 GMT  
		Size: 52.3 MB (52344739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ab22de89572f2f5b537ae4b33ef4de16dd2b7e8ca97166cf2663bdf8027260`  
		Last Modified: Thu, 07 Nov 2024 21:48:04 GMT  
		Size: 82.1 MB (82069310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47ee21093eca816e37e1238d15c7bb8febf98d9591119395fdeb7442c679637f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03409343673113cfdec1b8f0b84a30ce620af23b94f5a1a9f7b84e4eb79fc34`

```dockerfile
```

-	Layers:
	-	`sha256:a73d4798a1f7f0921b359f8d62345054f9a0c29ac05716eecb248f83a5581810`  
		Last Modified: Thu, 07 Nov 2024 21:48:01 GMT  
		Size: 5.2 MB (5184530 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f14222b2a31d35510cfaebc81137677c68217e1d09d4c6132743ffc9abba6d2a`  
		Last Modified: Thu, 07 Nov 2024 21:48:01 GMT  
		Size: 8.8 KB (8756 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e2bdfb8ad66728860c3598a7a00571e83822abdf355cc94400b68f515f144bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132889665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b7f0f8d4cccc610b2e4a4e2577e776c6f40f70aa5954910e81b743814c8aa86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ec853d5b361e3cd6830c71b2357ed2b7533d6c1f1c7f4859ea693c437e69991`  
		Last Modified: Thu, 07 Nov 2024 21:58:29 GMT  
		Size: 81.5 MB (81465664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24d64da78bd5418a21e4607164a7d53469d3cc4012cdabe5762bc5134f204066
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0664a92fa8a50fb139f4f4d32b21a41b01efef7bd0dc78c1305758f9f8c32eee`

```dockerfile
```

-	Layers:
	-	`sha256:8eff366fc0ca5a68dcf2632bd80bdaaab4d3909dac3971dfa3c4dc8743c77317`  
		Last Modified: Thu, 07 Nov 2024 21:58:26 GMT  
		Size: 5.2 MB (5183316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:739e2a0935864db74b13a4df2b9a521f2dd3ff7d15ee7c1d224620f068ec50c3`  
		Last Modified: Thu, 07 Nov 2024 21:58:26 GMT  
		Size: 8.8 KB (8836 bytes)  
		MIME: application/vnd.in-toto+json
