## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:45366ebe82704914b44033bcb32d830e9ee049dd65e35abdb55efdc8e9c1c440
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7bc1c3b8e5ec29230e6a05e711552df3ad3b2c166f05d17b72bc9d9df74e4aba
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135434347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ea186799750e9bf9f02fc75cca8927a0a7e2037cd08cee9b91a1fecb339ba5`
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
# Wed, 17 Apr 2024 00:01:17 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:01:17 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:01:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d15e367c8dd8c02d9bf042c967c6e9e3bf2425f0511798cf998fd8a59977665b`  
		Last Modified: Wed, 17 Apr 2024 00:20:24 GMT  
		Size: 83.1 MB (83110442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d5054fa9bc6b550080e23f0ed04d4bbb3551225e044dd7a3e16f5c5871f50dac
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133849651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3653d52582c170b9be097487828cfeabe1e3585f2b68be09d49575c002d3a429`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:10:07 GMT
ARG version=17.0.11.9-1
# Wed, 17 Apr 2024 00:10:07 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:11:04 GMT
# ARGS: package_version=1 version=17.0.11.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:11:05 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:11:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b26c9e5f7fa45e1043462e56b479d831daf4d191c707cc80fa1a9d0efa32842`  
		Last Modified: Wed, 17 Apr 2024 00:29:53 GMT  
		Size: 82.4 MB (82441326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
