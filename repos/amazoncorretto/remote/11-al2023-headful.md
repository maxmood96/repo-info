## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:0e477bf324f2912c7af04c5d67ccb19ebc2f9272131e7812c17913bf0f759c9b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff9d17c681c3c3f13584a7084fe8accbbba86bf1e303286fcb4a4f997de58460
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129166996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fad1adac3167ba750e5329cc65d46b6b897cfc5ddec709564d0e0f4bdbd2597f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d6f07a4c10a78dc230bb1bc2582e93fdd808a2b79539a9b9e8a29b5a94b2e75a`  
		Last Modified: Tue, 23 Jul 2024 01:08:56 GMT  
		Size: 52.3 MB (52314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:250e162f1afeff836601a86daeb4383949389ef0272c61f84398662c4166df63`  
		Last Modified: Thu, 25 Jul 2024 21:02:20 GMT  
		Size: 76.9 MB (76852817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:26ce2cf6ecd2f0e88d01dd65eae93eb63c8284dd8660e177b6cc8859c3a937d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9a585194999c73130ecf45e511232e26cb97ff64ea03b14c894fe7833f4f27`

```dockerfile
```

-	Layers:
	-	`sha256:705df9af05017f7abad75cdf831bcf71b88658b0f051fa5334056e2fb16f6ca4`  
		Last Modified: Thu, 25 Jul 2024 21:02:18 GMT  
		Size: 5.2 MB (5222398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb96acce0a4152fc4fae6e5e50a19082b1d64788fef51ae8b1411f73d74a94fb`  
		Last Modified: Thu, 25 Jul 2024 21:02:17 GMT  
		Size: 8.8 KB (8754 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9f6324e2e8ef1dce5c3f7f7e8061d2c0e55495de35f6224d733fab53637deeba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.4 MB (127410891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d342a046f06ebd194e3fbeb2571b3c396546e17b9258f6f34f35a6a73b6a05a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:39:24 GMT
COPY dir:220d6cf9a8bc29f51f634eb7049d0f57bb8f90ed9e3e9047cc8b655deba42085 in / 
# Thu, 11 Jul 2024 21:39:24 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:cbddb8fcc56265c7d316c4886c5874790b5fbdc8ecff1d3b10689482ea2ef29c`  
		Last Modified: Thu, 11 Jul 2024 21:39:41 GMT  
		Size: 51.4 MB (51401138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c4d2879b2eb9d7f6dcbf219de064b88c72634a0c5172b3cb4e18dd87ffd71`  
		Last Modified: Thu, 18 Jul 2024 01:05:11 GMT  
		Size: 76.0 MB (76009753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ed789e130a9eea6b1c10d3fb7465163e1d97736c7677211989b2f43351edad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b205c4ebb14f8366e3e5870c61a5a1e925a807835c78c32d42cedaf64253cc68`

```dockerfile
```

-	Layers:
	-	`sha256:23e04d7915e4d4786bd5885dfadb68600dbd090e6f396de6422544e64e07fedd`  
		Last Modified: Thu, 18 Jul 2024 01:05:10 GMT  
		Size: 5.2 MB (5222018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23107d4a0deb9f4e2b4b58d5a5698bd76118e359e47e800809b755e04d8e60c`  
		Last Modified: Thu, 18 Jul 2024 01:05:09 GMT  
		Size: 8.8 KB (8838 bytes)  
		MIME: application/vnd.in-toto+json
