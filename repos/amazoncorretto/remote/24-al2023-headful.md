## `amazoncorretto:24-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b7f5a872c9d25cfe6e89899077417ab6000d895e15f93c18734df4640387c306
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f01c56273f2de354819ed8c8b44101a14ea2aa4749f082c9b80c81dc0ee05f1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158988975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cedc6d53cd5458206bb08986bcaadcdc0e5cef59635b26e6b33de143c7059f21`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e8e9bb5a7082f97b36a3883979f670fc8b31d48763f09d8150d60ff9e1a957`  
		Last Modified: Wed, 02 Apr 2025 00:02:08 GMT  
		Size: 103.1 MB (103081922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:660864c9c360793e52e634772840363ecca24212f61e301cf4d14baa4ac180c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472158 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d58ec4e80fe30dd529c1fc84bd1bffb99db9e0335b8e9fe93c4f11dcf2c8ad60`

```dockerfile
```

-	Layers:
	-	`sha256:b9d7ea2716d74080bc089a1ee2f69df3fb7ff2cdd7282369f0b432be7b00a699`  
		Last Modified: Wed, 02 Apr 2025 00:02:07 GMT  
		Size: 5.5 MB (5462903 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3153ee3ecb2e73c01e52d12c16912c9a0b6900353b717db71f3e9f77b884bce8`  
		Last Modified: Wed, 02 Apr 2025 00:02:07 GMT  
		Size: 9.3 KB (9255 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:962b56c62125914170b7fbcb22eb03141a97032f317722aa3809e25d2d6f3aef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157041989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5b1de68ea0ac42b282fc571068b3faa2db49a0e59f797c66440fc723179b82d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36-2
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36-2 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce3a1b3f4fe85199457c7a794de97ab6cb51bc5606e8de9e7d9a240a7f417d9c`  
		Last Modified: Wed, 02 Apr 2025 00:39:50 GMT  
		Size: 102.1 MB (102080980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d6ee9f121ec032d7244f4c4658dfafed55bf78f7c52ab19be83c5c44b87a1903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:254ec97e5dfea269351bcc84c7048b9d142afa39b41e9defbbf3ed5c3b45abd6`

```dockerfile
```

-	Layers:
	-	`sha256:0ccc73b45c504d6bab902a5be401344ed66aab74f1cc75aa8c7c201e2352097b`  
		Last Modified: Wed, 02 Apr 2025 00:39:47 GMT  
		Size: 5.5 MB (5461717 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afe09f3f811b22e9050a66f55ff97ef97f756e923f76f77eeeb0831101dbcc86`  
		Last Modified: Wed, 02 Apr 2025 00:39:46 GMT  
		Size: 9.3 KB (9346 bytes)  
		MIME: application/vnd.in-toto+json
