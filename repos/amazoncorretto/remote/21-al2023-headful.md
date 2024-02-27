## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:5c4474ffcb1d8ea103f95791a70073fc7764e1ae1e2b9255c5abaef1f834e45a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4f3a5aeb9799a5a8603ac62ca24cbfd30fd6b8f69912c15ef07871807a22f927
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.4 MB (142427742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c443ed472120efb6a54050d17385f897b34a9d9a2ffe4bf80b766cc254b06b8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 22:51:53 GMT
COPY dir:fa03cac066e59421bfc5bec4359b41f98285f388dfc0f4cb40cc2ee361147dfd in / 
# Mon, 26 Feb 2024 22:51:53 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:19:54 GMT
ARG version=21.0.2.13-1
# Mon, 26 Feb 2024 23:19:54 GMT
ARG package_version=1
# Mon, 26 Feb 2024 23:21:06 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:21:06 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:21:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44282aad88366be312d36c238e9ca4ffe91decff2a409adaa83a194f8f21ba6`  
		Last Modified: Mon, 26 Feb 2024 23:31:18 GMT  
		Size: 90.2 MB (90217563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:424f52c0eaac2d9834f9f0d2af5297b0e528bd8b785a2012d25799ec1e21965a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.6 MB (140598927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63fa604cac55886e43672091487565cc657676b59b1ae64f03f95eea39f48a4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 26 Feb 2024 23:06:14 GMT
COPY dir:88ec842b814e75896373c7b1d8c94efa3d5513a6afbc1d2caee968c5e9f50573 in / 
# Mon, 26 Feb 2024 23:06:14 GMT
CMD ["/bin/bash"]
# Mon, 26 Feb 2024 23:43:43 GMT
ARG version=21.0.2.13-1
# Mon, 26 Feb 2024 23:43:43 GMT
ARG package_version=1
# Mon, 26 Feb 2024 23:44:51 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:44:52 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:44:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f534013dbea5ef16c757c5298f993b98988a6e0833221735408a89b0a475dd63`  
		Last Modified: Tue, 20 Feb 2024 02:11:59 GMT  
		Size: 51.3 MB (51298242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f01356aedbda4ba997a90eadbefb4932211dab74fe0788d3da6cd68c03e3de0`  
		Last Modified: Mon, 26 Feb 2024 23:53:11 GMT  
		Size: 89.3 MB (89300685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
