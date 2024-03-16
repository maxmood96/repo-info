## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:707f9c414fe72ee7382ea9f7329823f708c15855a7067ec8ec1ef3c653f7fc79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c6a51aa866ef9a5bbcd51b153ebfe684c5569aec79108a3745af17192b570a38
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128405600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa1e33838390809c6c1b2b6ea14d260fdaa92d56e01c1aa92007c7a8672bd074`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 11 Mar 2024 23:50:11 GMT
COPY dir:d7da6e069b79aa8b51b20a889b996a9bea020932e2948f46e1e355ca42d78f77 in / 
# Mon, 11 Mar 2024 23:50:12 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 02:49:19 GMT
ARG version=11.0.22.7-1
# Sat, 16 Mar 2024 02:50:11 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 02:50:11 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 02:50:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:89b8a841604356b93248cef633e19448985a8a9e86277f3b31c2e3860eabe2ad`  
		Last Modified: Wed, 06 Mar 2024 01:18:19 GMT  
		Size: 52.3 MB (52337114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b32bf99bfb25f76495031ee594e9fb7044a017b51b1bf281d80b186595fd9a46`  
		Last Modified: Sat, 16 Mar 2024 03:07:14 GMT  
		Size: 76.1 MB (76068486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:35cded2973b0640840d3d04ba41146578344789130432529f522bd963cb3df68
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126652489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8a98b1269bba70368584e645a8a1397dc499962a3f58cd7ab216861343acadf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 00:05:49 GMT
COPY dir:df28b18edcce192f5e6601a1f5352535de64369eb71fe3f006ea8b6aa29b9c84 in / 
# Sat, 16 Mar 2024 00:05:50 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 03:39:44 GMT
ARG version=11.0.22.7-1
# Sat, 16 Mar 2024 03:40:26 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 03:40:27 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 03:40:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:dd798988746a347b32a9e843088ef9c56978b6beca831a29a02bcd2ca002cea1`  
		Last Modified: Wed, 13 Mar 2024 20:11:17 GMT  
		Size: 51.4 MB (51414586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ded6319406991a33dd78427781f42a0d2bedf06031b270927d7f3b549221be62`  
		Last Modified: Sat, 16 Mar 2024 03:54:15 GMT  
		Size: 75.2 MB (75237903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
