## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5a6613537b0ddc16fb08a3b27241608751f14272e889ea9a052b84936139a07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5846ecc0fd6ee75feb6e1531865dda9ca1c833e50f26a4872e9291728177e736
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.5 MB (134541536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69d4ad12817050beb404b936d578005798c588078c344b2e9bbb9d7d48846b4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:20:25 GMT
COPY dir:c497d3c24209ef7d81f9c5abb7b10467dadda6adcaf860be5c03baaf83b5e43b in / 
# Tue, 28 Mar 2023 18:20:26 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 18:23:55 GMT
ARG version=17.0.7.7-1
# Thu, 20 Apr 2023 18:23:55 GMT
ARG package_version=1
# Thu, 20 Apr 2023 18:24:33 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Apr 2023 18:24:33 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:24:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:ee5c3b4d09bc9dd7590b7480cb385347f445a9fa73056b912cc9ed67ce54d0ce`  
		Last Modified: Fri, 24 Mar 2023 03:10:39 GMT  
		Size: 52.3 MB (52255843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32ed304ed9fc35bb60dcfa2d27e2397c0a50bbd99e599f8373f05a3213fbda8`  
		Last Modified: Thu, 20 Apr 2023 18:35:16 GMT  
		Size: 82.3 MB (82285693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6973f5dc5990896afc4152c98c561031795cdf830b44de996ae05877696757d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132896621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f261fbb20e0a99d61cb968cf7b4856d3cac3de84e5616d3b9183c74735d2e14`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 28 Mar 2023 18:39:52 GMT
COPY dir:0b162ee66bcb569c55f662aaca3ee7fff9bf5a498748208a280de7797569e5dc in / 
# Tue, 28 Mar 2023 18:39:53 GMT
CMD ["/bin/bash"]
# Thu, 20 Apr 2023 17:43:09 GMT
ARG version=17.0.7.7-1
# Thu, 20 Apr 2023 17:43:09 GMT
ARG package_version=1
# Thu, 20 Apr 2023 17:43:45 GMT
# ARGS: package_version=1 version=17.0.7.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 20 Apr 2023 17:43:46 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:43:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3a410071be52fec7335cb666804896319a1ac81ef15af4c0f1302ffe8834b63f`  
		Last Modified: Fri, 24 Mar 2023 03:10:43 GMT  
		Size: 51.3 MB (51297211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3301dd810923ce1a682e7af077c1cd4a35b7f707a05a734f3c5d362804552da7`  
		Last Modified: Thu, 20 Apr 2023 17:53:56 GMT  
		Size: 81.6 MB (81599410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
