## `amazoncorretto:11-al2022-RC-headful`

```console
$ docker pull amazoncorretto@sha256:2b4886c4a73cde72b4a77a7fa8e6c75f2e1853fc993024d13e346c1e690d5d7f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2022-RC-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3c6518afd2730856c12573272433224795bf9206519fb85a33b4ee4764a8c5a1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133058611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c294164253922dbfd4ffbfb8a8c940801fa9e85957f6aa87e1f8a96119e56554`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 01:21:07 GMT
ADD file:c2f3cc504734106dfe39dce615cfa085097451f0876c9574a8294c8494624c9f in / 
# Fri, 16 Dec 2022 01:21:07 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 02:14:57 GMT
ARG version=11.0.17.8-1
# Fri, 16 Dec 2022 02:16:12 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2022.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2022.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 16 Dec 2022 02:16:12 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 02:16:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f692b7ceefbf778187c80c39b96d604e39ccf4a889e08c5f052481134db22ae1`  
		Last Modified: Tue, 13 Dec 2022 16:21:44 GMT  
		Size: 57.9 MB (57867562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38af1a86303bbe9edbd2364f6ee0b52596923b52a04ff7f7f87d03f4b0f8fcd`  
		Last Modified: Fri, 16 Dec 2022 02:23:25 GMT  
		Size: 75.2 MB (75191049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2022-RC-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c088b6faa602698a29d93d1e8ab7fff8d952e9918c8177f5b9df99cd53caa374
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131169597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b531e835d3ead281822bfbd56be180d79e279658176d5ccd0e75fd701ab911b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 16 Dec 2022 00:41:37 GMT
ADD file:ff147b37fd20344db08d3808c57eecb4baf220c236bdadf01d19a61f2dd6327e in / 
# Fri, 16 Dec 2022 00:41:38 GMT
CMD ["/bin/bash"]
# Fri, 16 Dec 2022 00:59:47 GMT
ARG version=11.0.17.8-1
# Fri, 16 Dec 2022 01:00:34 GMT
# ARGS: version=11.0.17.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2022     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2022.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2022.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 16 Dec 2022 01:00:35 GMT
ENV LANG=C.UTF-8
# Fri, 16 Dec 2022 01:00:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f3bff8cbe57b20ad8a63095a2b0c5d31afccc39fd7fbaab9b0c483430b38429a`  
		Last Modified: Tue, 13 Dec 2022 16:26:02 GMT  
		Size: 56.7 MB (56712057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a35baef9ae15f472f3e21c00183b9a4127b63959bce170c04410f2a92de774c0`  
		Last Modified: Fri, 16 Dec 2022 01:04:44 GMT  
		Size: 74.5 MB (74457540 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
