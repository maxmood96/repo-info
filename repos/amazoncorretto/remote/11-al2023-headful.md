## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:81a20cacc55dfa995f05d5de55b5981b5dc22ad4e960e2604e49563463a9a122
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:27bbc74e8c3e2beda143d3773e20732603d1c4c05ee999c940aa07c705aafcfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129166575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccfb064089973db0d249c87459572bcd3acd566a6acef605237b13f49e1a733`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 10 Jul 2024 20:01:54 GMT
COPY /rootfs/ / # buildkit
# Wed, 10 Jul 2024 20:01:54 GMT
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
	-	`sha256:f03636e672ba797137f2f72e64c7fdf7947397c0880ca5f9e9962a85462a7875`  
		Last Modified: Thu, 11 Jul 2024 02:05:27 GMT  
		Size: 52.3 MB (52313836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:316b8567ae55d203c6c5ed120f2b9a52f65d2e96c98f0057c6c35aea2b14bb6c`  
		Last Modified: Tue, 23 Jul 2024 00:07:34 GMT  
		Size: 76.9 MB (76852739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba35d576293a9c95e18454b18ad04fe71c954b9c8e342304b73622a3a084b086
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c958ed1666d93deb193cc8655d66310c92e9237e50caeb8b841e31d8fd690a7c`

```dockerfile
```

-	Layers:
	-	`sha256:d99fbc4878dca0aea87e97fbcfb22a4923c1722f1c7b00edf9e768ffc17f6274`  
		Last Modified: Tue, 23 Jul 2024 00:07:32 GMT  
		Size: 5.2 MB (5222398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27735dcbd32b1290bdb02a89e39b854245090203089ec1e83218c67fddff2611`  
		Last Modified: Tue, 23 Jul 2024 00:07:31 GMT  
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
