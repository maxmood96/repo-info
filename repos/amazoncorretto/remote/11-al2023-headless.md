## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2251663364120506240dae6a9e8e4df1225841065b227db98338e24b23b12004
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:849d75a0268cc34c14a30dad1521009cfff1e6ae93b304a80385d9a7eee987eb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128401662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc4a55930c1137d1bd040b38d8e8094db623496d8c3059b3bfb86664135161e4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Sat, 16 Mar 2024 07:58:56 GMT
COPY dir:a3b34d0fa41c44f27db0e1cc5fb85c42e2d376f97e37c993883bc79b0ac16bdc in / 
# Sat, 16 Mar 2024 07:58:56 GMT
CMD ["/bin/bash"]
# Sat, 16 Mar 2024 13:34:42 GMT
ARG version=11.0.22.7-1
# Sat, 16 Mar 2024 13:35:26 GMT
# ARGS: version=11.0.22.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Sat, 16 Mar 2024 13:35:26 GMT
ENV LANG=C.UTF-8
# Sat, 16 Mar 2024 13:35:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:47a7782bf36730e29aeeeb2bd36b1fc2a9d8b97f2ee4990a6ad2300602de69b0`  
		Last Modified: Wed, 13 Mar 2024 20:11:15 GMT  
		Size: 52.3 MB (52334338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1af4389a2da720928d0057cf32cf033adce8c9577207a05a6b726d126603a2`  
		Last Modified: Sat, 16 Mar 2024 13:47:09 GMT  
		Size: 76.1 MB (76067324 bytes)  
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
