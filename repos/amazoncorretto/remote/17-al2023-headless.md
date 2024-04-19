## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:965f13c414ad27d99fc1529a77ff7caff933388c521b6b4c99710381bd34f0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0b06e1c125937ae5b0708d3110e925e857bd470ea5df042f59dcd5590fe4aab9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134750082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:997b424c82817ab0a6be8ae19d2c55625fa544426347b8eba4ca5bc0f035d6ae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:00:10 GMT
ARG version=17.0.11.9-1
# Wed, 17 Apr 2024 00:00:11 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:00:55 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:00:56 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:00:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:285617a00a257b52cfa3174528cf68b0ef29a9c938f07e3f422aeacdf79bda47`  
		Last Modified: Wed, 17 Apr 2024 00:20:05 GMT  
		Size: 82.4 MB (82426177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:82447711927e5e7d3ba999e3e5f8b2ad93e4d636a775f14ec7ccdaa303b77674
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133161564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:983203477d2eb76631e2b51ff6c8d04828127c880f469b916771429e4ddd7e52`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 19 Apr 2024 22:10:28 GMT
COPY dir:e8d306065b89c24e8d7ed76b1f4a499224cd18e3ec44dc6823b5d039220ebc19 in / 
# Fri, 19 Apr 2024 22:10:29 GMT
CMD ["/bin/bash"]
# Fri, 19 Apr 2024 22:33:17 GMT
ARG version=17.0.11.9-1
# Fri, 19 Apr 2024 22:33:17 GMT
ARG package_version=1
# Fri, 19 Apr 2024 22:33:54 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 19 Apr 2024 22:33:55 GMT
ENV LANG=C.UTF-8
# Fri, 19 Apr 2024 22:33:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0fff0db406e493d5737bccd8db4b9460e6d6c5e6d45f62e14ae7cb208fcc984a`  
		Last Modified: Fri, 19 Apr 2024 22:11:04 GMT  
		Size: 51.4 MB (51413307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2af93fb85c85bc2738adf652ead17c1f02b1cdb06614105449284b3ff1863af`  
		Last Modified: Fri, 19 Apr 2024 22:44:53 GMT  
		Size: 81.7 MB (81748257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
