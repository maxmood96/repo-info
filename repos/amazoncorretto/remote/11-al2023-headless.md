## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2f12e71f49cf11340604b024120dc65a0ac1bd57f1640a914ed1ae895d616047
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d3afeae870caf48a53c5f62e02c7c56bebb379149aa7efdc049f138f6470e982
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.3 MB (128305315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d42f95d9725984dbee8656c4494484870b7aa43391e7e9d7c7f5e1ec2c676d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Feb 2024 23:53:41 GMT
COPY dir:a483dadf03df21b4c46ae05c4564496c155a45055f49c3293b4e7554c8160845 in / 
# Thu, 01 Feb 2024 23:53:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:38:47 GMT
ARG version=11.0.22.7-1
# Fri, 02 Feb 2024 00:39:27 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 02 Feb 2024 00:39:28 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:39:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:567d8ee5457ce911a8659b74a8187fbe402d4417070b8c4af0bf7d6289c1baae`  
		Last Modified: Thu, 01 Feb 2024 00:30:11 GMT  
		Size: 52.2 MB (52245559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a425f0072059c55e94eb3925ea04c9b4131f066c677ad64dee75f91e95ef0111`  
		Last Modified: Fri, 02 Feb 2024 00:51:25 GMT  
		Size: 76.1 MB (76059756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bf7f94d8efabe8511be211814aeb044767c64dea119cb4b42557d1550f9ab7b7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.6 MB (126555101 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f09c99104759aea3f724f71946cbd1c62d9380858828b366dbb123f51c9a1f64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:30 GMT
COPY dir:da17a174bd602e575391d08ca94d5595606a8d6d7b3b957cdec78f5fad499e19 in / 
# Thu, 01 Feb 2024 23:30:31 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:49:38 GMT
ARG version=11.0.22.7-1
# Thu, 01 Feb 2024 23:50:15 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 01 Feb 2024 23:50:16 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:50:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:d111cbc02b249a552b77e87298e3df2ce29173bc39b7d82aecba5ca8a2ab06d2`  
		Last Modified: Thu, 01 Feb 2024 00:30:08 GMT  
		Size: 51.3 MB (51322438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b874f05895c4a31f9a2d0fd7ffa1a066e5991631834091f2a1865636e36d99c`  
		Last Modified: Fri, 02 Feb 2024 00:00:09 GMT  
		Size: 75.2 MB (75232663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
