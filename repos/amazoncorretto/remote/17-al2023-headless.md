## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b698a6fe9f427a3c44bb8b90f176f30f95fca199f397e20293a4e93d600cf50c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:83f658133dca87634b6fe88f31bb7e59b2b2a0bef30658212ef57ec22bce7260
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134738715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b9e8431617f041bf484285337100a274be56447a958596d93ead81559d4e70d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:26:32 GMT
COPY dir:7cf66bb9a4300419df5b669628ccf58a30d02fe56dd9811e6baaca920acf962f in / 
# Wed, 05 Jun 2024 00:26:32 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:41:42 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:41:42 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:42:28 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:42:28 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:42:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f6175f9c503b77e6cec852666a7133ed71ff16fd23342bcc58c01fa48948b06f`  
		Last Modified: Tue, 28 May 2024 21:59:02 GMT  
		Size: 52.3 MB (52320215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d7ac49cf65c242bfb42727fdd31508e2e28e662224b82edb36d8a4a9d875bf`  
		Last Modified: Wed, 05 Jun 2024 02:55:14 GMT  
		Size: 82.4 MB (82418500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:409b1c27b34e716d61969bba140eca5ff2bc5fad3b136f92a6aa20b1481878a7
```

-	Docker Version: 23.0.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.1 MB (133137856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9108852071f1cc01d549e333b3ee177b293c5ad5cf675ed8910dda77fa0d383`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 05 Jun 2024 00:47:28 GMT
COPY dir:ba9790f78add1c4638ee46d842ce6b7ee4d659e1ce4ca5bfa2485adaf6cac8ec in / 
# Wed, 05 Jun 2024 00:47:29 GMT
CMD ["/bin/bash"]
# Wed, 05 Jun 2024 02:33:25 GMT
ARG version=17.0.11.9-1
# Wed, 05 Jun 2024 02:33:25 GMT
ARG package_version=1
# Wed, 05 Jun 2024 02:34:03 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 05 Jun 2024 02:34:04 GMT
ENV LANG=C.UTF-8
# Wed, 05 Jun 2024 02:34:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:decbb28a26fad91fa4c617ae5541ffaa8f680fc91855c8bb640254519df67bf1`  
		Last Modified: Wed, 29 May 2024 02:10:34 GMT  
		Size: 51.4 MB (51403878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2661fc71123dcf3af8ca953ad9f8cef60c926001378885b842b79e9717a64772`  
		Last Modified: Wed, 05 Jun 2024 02:44:28 GMT  
		Size: 81.7 MB (81733978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
