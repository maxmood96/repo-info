## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b1be234f2cef949867624033a9fd5f25e39ecd1e45542052b05a3e7dbde6c729
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d6e76fcab3c95c1b20378bdf0b73ea0c3206b48ef8d09c15dda36d6c251f2e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.2 MB (129166596 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23b3e0e04020350cf15aefd0089257079556cc7b36eabb8e45ccbaa1d1fe4811`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Jul 2024 21:19:33 GMT
COPY dir:8edd892881e79c0c11996c1a60e2c04d066537e06bdf88e1def994a6148ea23c in / 
# Thu, 11 Jul 2024 21:19:33 GMT
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
	-	`sha256:ee5ee70789863a32f444d11d47a2849acfc6089e3e8c78d196f63475ee994293`  
		Last Modified: Thu, 11 Jul 2024 21:19:58 GMT  
		Size: 52.3 MB (52313695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122da507d98c9e32631cd221f0930cf83e8795cf52585016af22aa43be7fdded`  
		Last Modified: Thu, 18 Jul 2024 00:55:51 GMT  
		Size: 76.9 MB (76852901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4d4f8469844ceed65263978e3bb9082b16ce69d714ee12375283e249e110ce7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88449cfb3dd0ec7e8a452f55cf4201b8309997c045120b4ef894ff87df78cecd`

```dockerfile
```

-	Layers:
	-	`sha256:af1b40e396512309caed31c52d3ce1d70199a8ef19a501e87a99b809d436fdda`  
		Last Modified: Thu, 18 Jul 2024 00:55:50 GMT  
		Size: 5.2 MB (5222398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:df5cc7c0d56d56ffca7e23ddde607b0b4174872ea5c6e8d073b95e740c6d401a`  
		Last Modified: Thu, 18 Jul 2024 00:55:50 GMT  
		Size: 8.6 KB (8558 bytes)  
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
