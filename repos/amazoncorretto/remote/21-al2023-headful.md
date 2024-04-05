## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:7955d623b7da40572b7bee04873e167bf8e3c1bc2d628edb66c353895d232c84
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:526be4fe4bd340bd7b471ccc2421a2d9f1a03a533f61049bce68e44e8e11ab00
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.5 MB (142537505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29a2dc401c589b58baa8f511ccf3f4bd7c8e39235879f3e1f84e524a0b588444`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:30:35 GMT
ARG version=21.0.2.14-1
# Fri, 05 Apr 2024 19:30:35 GMT
ARG package_version=1
# Fri, 05 Apr 2024 19:31:42 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 19:31:42 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 19:31:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96b096c93023478f5155f47bedadce9c61f65ba6d9189f2ce113ee22a754af2d`  
		Last Modified: Fri, 05 Apr 2024 19:43:43 GMT  
		Size: 90.2 MB (90213600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:afd70a0dbbcd9bb496472ce074c1cbe14cc23f51d891676dd29bb20f8cca4f49
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.7 MB (140703240 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b5e42c197714a5b35cedd54ba39f2c620259ec1257115335034bb0f8ebd3e24`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:51:18 GMT
ARG version=21.0.2.14-1
# Fri, 05 Apr 2024 18:51:18 GMT
ARG package_version=1
# Fri, 05 Apr 2024 18:52:20 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 18:52:21 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:52:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ba5c05f1add8eeaeb3ab73dbe0975a4251fa98daa6f3fe870fd9747cf862bb4`  
		Last Modified: Fri, 05 Apr 2024 19:02:33 GMT  
		Size: 89.3 MB (89294915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
