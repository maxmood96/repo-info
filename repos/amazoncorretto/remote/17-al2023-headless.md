## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:cd5f1a56d0f0b54057679116a01d16aec8e3a977e35b96a04516e48d88cd4a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:edf649641095d2acd7e5f9357b79d9d730cfa7404bbf979f7996feeab38e6ad8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134540531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bf50e9091ca0cb9e03411b6fd3a9a26d636383af1fcd07ddad55c03665447c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:51:53 GMT
COPY dir:fa03cac066e59421bfc5bec4359b41f98285f388dfc0f4cb40cc2ee361147dfd in / 
# Mon, 26 Feb 2024 22:51:53 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:15:24 GMT
ARG version=17.0.10.7-1
# Mon, 26 Feb 2024 23:15:24 GMT
ARG package_version=1
# Mon, 26 Feb 2024 23:16:15 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:16:15 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:16:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6ba694aac6bd1cad13233d584cbeab7c42c370f18a93c7a6bc1088ff2cf1021`  
		Last Modified: Mon, 26 Feb 2024 23:28:12 GMT  
		Size: 82.3 MB (82330352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:369a7dd8c21ab3a0c4c283ecce4ae6eb90ea13f1190aa90d3f39453c8f7f7e05
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.0 MB (132967288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f7ae783d762a76d1c10ff018d76eac3e37155a1640c4928ca09897ef63f40f7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:14 GMT
COPY dir:88ec842b814e75896373c7b1d8c94efa3d5513a6afbc1d2caee968c5e9f50573 in / 
# Mon, 26 Feb 2024 23:06:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:40:26 GMT
ARG version=17.0.10.7-1
# Mon, 26 Feb 2024 23:40:26 GMT
ARG package_version=1
# Mon, 26 Feb 2024 23:41:08 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:41:09 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:41:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f534013dbea5ef16c757c5298f993b98988a6e0833221735408a89b0a475dd63`  
		Last Modified: Tue, 20 Feb 2024 02:11:59 GMT  
		Size: 51.3 MB (51298242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65914af3af9079b27c0fc87fa2920c31b3d9b146b30d898fac48da5309bd2295`  
		Last Modified: Mon, 26 Feb 2024 23:50:34 GMT  
		Size: 81.7 MB (81669046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
