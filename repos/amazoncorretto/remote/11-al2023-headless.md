## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:0bf977d7f99a5c9451cc64d05bbd9312d34e81dd2c79ae2d63d893dcdd992f4d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f220e86f574c443ce721cac427bc944962f301b1bf70e85a7643fbd0e326383b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128519661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a13f9f5f497089de3e965e019569801977c013ca0b71f3ab746e7f462c26393`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:42ce99aa0f68a7f3dc752dad87f21431a084b94a3818ff00f932236a9010d564`  
		Last Modified: Tue, 15 Oct 2024 02:06:15 GMT  
		Size: 52.3 MB (52343832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8310f6406b73caf9563eabb440dbdbfbd55ddbed9508371f07fe071689bb3bf`  
		Last Modified: Mon, 21 Oct 2024 18:57:13 GMT  
		Size: 76.2 MB (76175829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a6ac3612ffe4879d8a5cccc94b14f7ad0483c570764f0809ee1fdecb792fe53e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8999e75fe3476c442001bf534d9e96e99f13f6a2afc793e2a28de169cdccca`

```dockerfile
```

-	Layers:
	-	`sha256:0e858b83283f70ff7f79e049db50de1b24a032a92658ad8e8e51b386bb4691f8`  
		Last Modified: Mon, 21 Oct 2024 18:57:11 GMT  
		Size: 5.2 MB (5198470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb24fa4289d45e1992c16b25eb9d4bf47f4cd6a43fa99a6858d92c211cbf694`  
		Last Modified: Mon, 21 Oct 2024 18:57:10 GMT  
		Size: 8.7 KB (8650 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e21becad189c354cb621d70b2c4731696da09da2c117a7abaa17e5acd3299eb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.8 MB (126790479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bee6aa7445ed08f1d81a491e6055cb3ca1188cec86843dc6212aef6e69b435eb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9-1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:923a2071aa1c62af0f57aa46e86e64587ba93da0a38eaf52d228227154730e17`  
		Last Modified: Tue, 15 Oct 2024 02:53:59 GMT  
		Size: 51.4 MB (51424527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08430701df4209769e99d12624242e753be0d9bb455dd25c279b3d940b823f6`  
		Last Modified: Mon, 21 Oct 2024 20:59:32 GMT  
		Size: 75.4 MB (75365952 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c9ccd7c9fbe54fa8d34d20f03594983497a3f2b8ad7b634a4e032e055918d881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5206819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61bf31826353b72a230ab3d379fba856f9a2e4ae83c7afff94882de42867ac8e`

```dockerfile
```

-	Layers:
	-	`sha256:31ec166c0b158a8a0f1cda9b5a0298e886c21e418c48e878091491ae6accd661`  
		Last Modified: Mon, 21 Oct 2024 20:59:29 GMT  
		Size: 5.2 MB (5198087 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c558b8f4bac2e25c4065ad0c54e1029781ba104dee34c826a45e53c70dcc24b8`  
		Last Modified: Mon, 21 Oct 2024 20:59:29 GMT  
		Size: 8.7 KB (8732 bytes)  
		MIME: application/vnd.in-toto+json
