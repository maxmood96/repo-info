## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:21559128c3c0e0fdcff3b951132b1743cb8e2d526b6893e6536426e40071d15a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7bc43ab36968e75f78ffafb0ffb4e900aab147f1ce418da3784072277d59731
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.2 MB (135224558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db2bf8ac068de498720505e59d4aadaa962028664557d857c77d0ab02d0e2b09`
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
# Mon, 26 Feb 2024 23:16:36 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:16:37 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:16:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:8784573bb84d178812057375084b2df4e8a0ffb22734f522709063f9581c296f`  
		Last Modified: Tue, 20 Feb 2024 01:09:31 GMT  
		Size: 52.2 MB (52210179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48d2576641e3136b73cb29a4f03569ea95a7e749e41f5b5453cc05e5c44682a3`  
		Last Modified: Mon, 26 Feb 2024 23:28:30 GMT  
		Size: 83.0 MB (83014379 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e5624b196cf3c1f46d57f62d5e880132a17c22af38cb2f86279bd279e8db8d6d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.7 MB (133659899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b3dd9558f151da56aec9a824aacc71c8a865c2dcce47dafc8477e86750529ed`
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
# Mon, 26 Feb 2024 23:41:24 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 26 Feb 2024 23:41:25 GMT
ENV LANG=C.UTF-8
# Mon, 26 Feb 2024 23:41:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f534013dbea5ef16c757c5298f993b98988a6e0833221735408a89b0a475dd63`  
		Last Modified: Tue, 20 Feb 2024 02:11:59 GMT  
		Size: 51.3 MB (51298242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe101098a4bc2e70a2d69d979b758fdf2dc0b7d11feda528311fb3b454142b4`  
		Last Modified: Mon, 26 Feb 2024 23:50:50 GMT  
		Size: 82.4 MB (82361657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
