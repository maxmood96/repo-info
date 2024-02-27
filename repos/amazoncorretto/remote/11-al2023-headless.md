## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ceb56d592ac6fc0800792978ab1eebb7a4cbc9ff302d19b8a91dd8fd5c1ce784
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:074c0003d62bc23e5bb7f4015f349bf3a6dddc7b6eeae2f3840e39270620e272
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128265257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4f2e42b02d0301b82a46bf20a49b3b8908945ae696319a4210e7345570815e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:51:53 GMT
COPY dir:fa03cac066e59421bfc5bec4359b41f98285f388dfc0f4cb40cc2ee361147dfd in / 
# Mon, 26 Feb 2024 22:51:53 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:11:59 GMT
ARG version=11.0.22.7-1
# Mon, 26 Feb 2024 23:12:44 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:12:44 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:12:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:511d2abb3dd937fb95ebcd6bec2a2815cc0be3c96a0b42075c86e63ecc562322`  
		Last Modified: Mon, 26 Feb 2024 23:25:50 GMT  
		Size: 76.1 MB (76055078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:de4eff47d9e4a3fd6c77e47773a8187428a5214a34fc2165ad1b4df44bda803d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.5 MB (126532006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67952c2326a79b0c8aaf21ded9c02ac190e3c13c0d6bb41e5803697d3316d36e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:14 GMT
COPY dir:88ec842b814e75896373c7b1d8c94efa3d5513a6afbc1d2caee968c5e9f50573 in / 
# Mon, 26 Feb 2024 23:06:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:37:53 GMT
ARG version=11.0.22.7-1
# Mon, 26 Feb 2024 23:38:30 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:38:31 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:38:31 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f534013dbea5ef16c757c5298f993b98988a6e0833221735408a89b0a475dd63`  
		Last Modified: Tue, 20 Feb 2024 02:11:59 GMT  
		Size: 51.3 MB (51298242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45621a5897879c7a1960e97b5793864aa533d809b5a35e2480d758d7431bf0aa`  
		Last Modified: Mon, 26 Feb 2024 23:48:31 GMT  
		Size: 75.2 MB (75233764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
