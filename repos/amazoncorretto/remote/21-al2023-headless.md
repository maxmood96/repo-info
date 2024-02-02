## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:1bbd3b67d2aea90f744a7b2215776fc4ceca2d7f7b866bcdb617911893a58b93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32c1c129199dd593f80d18a1f89f63396acfa42b9c8af16bc26893eae890fa2f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141760387 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ef73b13fe68b4a1155295e215886f14655384cc98b02a49da9928152eb63792`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Feb 2024 23:53:41 GMT
COPY dir:a483dadf03df21b4c46ae05c4564496c155a45055f49c3293b4e7554c8160845 in / 
# Thu, 01 Feb 2024 23:53:41 GMT
CMD ["/bin/bash"]
# Fri, 02 Feb 2024 00:45:56 GMT
ARG version=21.0.2.13-1
# Fri, 02 Feb 2024 00:45:56 GMT
ARG package_version=1
# Fri, 02 Feb 2024 00:46:40 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 02 Feb 2024 00:46:41 GMT
ENV LANG=C.UTF-8
# Fri, 02 Feb 2024 00:46:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:567d8ee5457ce911a8659b74a8187fbe402d4417070b8c4af0bf7d6289c1baae`  
		Last Modified: Thu, 01 Feb 2024 00:30:11 GMT  
		Size: 52.2 MB (52245559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bb8165693bdb2b332e175ca315bb57b19f4ea007362bfb02bfe8971f67c0e1d`  
		Last Modified: Fri, 02 Feb 2024 00:56:26 GMT  
		Size: 89.5 MB (89514828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:54ec513ca64efbd558d9119ddd646432dd17ccf645e32c098f4244869754368e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.9 MB (139895167 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0483dd6f3daaaf242bd414ae5ccc341fa4cf4065821d320555def4d43b7470d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 01 Feb 2024 23:30:30 GMT
COPY dir:da17a174bd602e575391d08ca94d5595606a8d6d7b3b957cdec78f5fad499e19 in / 
# Thu, 01 Feb 2024 23:30:31 GMT
CMD ["/bin/bash"]
# Thu, 01 Feb 2024 23:55:26 GMT
ARG version=21.0.2.13-1
# Thu, 01 Feb 2024 23:55:26 GMT
ARG package_version=1
# Thu, 01 Feb 2024 23:56:04 GMT
# ARGS: package_version=1 version=21.0.2.13-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Thu, 01 Feb 2024 23:56:05 GMT
ENV LANG=C.UTF-8
# Thu, 01 Feb 2024 23:56:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:d111cbc02b249a552b77e87298e3df2ce29173bc39b7d82aecba5ca8a2ab06d2`  
		Last Modified: Thu, 01 Feb 2024 00:30:08 GMT  
		Size: 51.3 MB (51322438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a0d69384eae2eba099e8996f02c6a45936f24edc3f81e5af98747e22e0741`  
		Last Modified: Fri, 02 Feb 2024 00:05:05 GMT  
		Size: 88.6 MB (88572729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
