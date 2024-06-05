## `amazoncorretto:22-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:6e57bc8bac28bb1e29a59fd75b4cfce9d77783db3ed5452ea5f58d3c1277a8d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fb3d72997798dfeb6978aabedce8be492adb4f0b3b33523b8838cfac1552c213
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.9 MB (140920738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac0bcaed6a8fc6b75643d63021cc2e5525b04b2768666c76ce9ada2a4733bf9`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:26:32 GMT
COPY dir:7cf66bb9a4300419df5b669628ccf58a30d02fe56dd9811e6baaca920acf962f in / 
# Wed, 05 Jun 2024 00:26:32 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:47:10 GMT
ARG version=22.0.1.8-1
# Wed, 05 Jun 2024 02:47:10 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:47:56 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:47:57 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:47:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:f6175f9c503b77e6cec852666a7133ed71ff16fd23342bcc58c01fa48948b06f`  
		Last Modified: Tue, 28 May 2024 21:59:02 GMT  
		Size: 52.3 MB (52320215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:498ad08fccdde27465f2bc5764e5b06d3410736040ae7141cc6f7b124c03a313`  
		Last Modified: Wed, 05 Jun 2024 02:58:59 GMT  
		Size: 88.6 MB (88600523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6c263c1d51590d9fdc8224c8e8633a4e405b432a362ad3ce3bd4ff97fa21452a
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.0 MB (138956671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c559022856ba08e93f49995e00aefdb99c6a930f811a90a778ebb6b309bdef4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:37:36 GMT
ARG version=22.0.1.8-1
# Wed, 05 Jun 2024 02:37:37 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:38:25 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:38:26 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:38:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:269afa861639601479efc5a1ed8a54eabd15bfdc1969d4003faebe112ee7429e`  
		Last Modified: Wed, 05 Jun 2024 02:47:46 GMT  
		Size: 87.6 MB (87552793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
