## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:212d31e5fd73180b8d8b03f94bbf40392f44b0eb97eed86c881840ac05b92845
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
$ docker pull amazoncorretto@sha256:f6d9bdea9702a60a32c0a69b4f9cb7026cc379c8862884e7ab537bf5d46eb2b4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133075608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12045a07ef91380a176a7437f93dd21b3018f1e8b814feffd0ff8bc6c271dcd4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 22:39:43 GMT
COPY dir:2bac3e0f2f9808be2259a0eea507562cc31d6f7cf5f26809139e8bb63fb6b535 in / 
# Mon, 11 Mar 2024 22:39:44 GMT
CMD ["/bin/bash"]
# Mon, 11 Mar 2024 23:14:50 GMT
ARG version=17.0.10.7-1
# Mon, 11 Mar 2024 23:14:50 GMT
ARG package_version=1
# Mon, 11 Mar 2024 23:15:27 GMT
# ARGS: package_version=1 version=17.0.10.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Mon, 11 Mar 2024 23:15:28 GMT
ENV LANG=C.UTF-8
# Mon, 11 Mar 2024 23:15:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:89bff426afee4c835c6855932ea2864aef333271964dcfe8c4e0cd4be90649f8`  
		Last Modified: Wed, 06 Mar 2024 01:18:22 GMT  
		Size: 51.4 MB (51406909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e746c61231ba714bf6f774835375b44eccd70bfec67eb4a0e22ca6c250e3105`  
		Last Modified: Mon, 11 Mar 2024 23:24:40 GMT  
		Size: 81.7 MB (81668699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
