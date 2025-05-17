## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:d0afbac74735b4918e6c865535945252145f76382d981165d11bf9f1285b3caa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:038490d4a985df6bc7ea2cd1f2b79acbbbd531911e25ed6caf107bcc4da313a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143623385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f057ab7a6a6c3db1b581a7b711aeb251b30a45979a0c9264a59c83b1b7ca2436`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:1c3112c87ab2d6209030c22629180b5d1958fca3765b3cbcfbc9bcfa1ee6e425`  
		Last Modified: Thu, 08 May 2025 17:04:44 GMT  
		Size: 53.9 MB (53880920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26be3ab9999222f0a3cc091c8ee6781923b3c587333853c70d50676fdda8d1b5`  
		Last Modified: Thu, 08 May 2025 18:27:19 GMT  
		Size: 89.7 MB (89742465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ca7d2694db3ee9d8cc29175c59a19b9972cea06924f42d873fa1c226d6e1874b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5204060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25316ad14ebf20563f156ae90386cd952138b0178769d6a95ee87a8b2f421a20`

```dockerfile
```

-	Layers:
	-	`sha256:eda396c92f8454a0db1f92c87f3eeb0c5b67b041c86c0151f63ebbde304906e5`  
		Last Modified: Thu, 01 May 2025 21:08:23 GMT  
		Size: 5.2 MB (5195133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36b3c2a63f06cee822b46cdc345e88182975a694a23fd43d42208f9147605a4c`  
		Last Modified: Thu, 01 May 2025 21:08:22 GMT  
		Size: 8.9 KB (8927 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:95fd06ddaa59a4ad432b57382932d36a6ccc136a6f56994a606be11aded1212a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.7 MB (141701597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d9a41c30c609d516c00bb25f230391033d7b1f4e64b0a34ff8b78be7303a67d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5804bd91a568b15c202af6e01f57d869865af0d532f8773d8faefb503ef0bbfe`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 52.8 MB (52811047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d0d7eeb630a127223041496cd42426091b448ef886f7626dce1d4d7a9ab53f`  
		Last Modified: Fri, 16 May 2025 23:54:45 GMT  
		Size: 88.9 MB (88890550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8bc2123e06f5c27e2aaf0ef0176355d339ffc4ae819a5f4a5eda5ae09dcda200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202932 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5089405fb3eba2e2903dcd49d25b3d886625f7a87459c6af74202d7edd9c5bf6`

```dockerfile
```

-	Layers:
	-	`sha256:aee9e5deaffbd7a6bb7cd4157aadca2a35fa4aa9c4b001f07aeef2c181c9c825`  
		Last Modified: Thu, 01 May 2025 21:24:21 GMT  
		Size: 5.2 MB (5193926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:024a73ffebaa139259d0b32145e6de8f42f6251d364902a0ad80c7e02021735c`  
		Last Modified: Thu, 01 May 2025 21:24:20 GMT  
		Size: 9.0 KB (9006 bytes)  
		MIME: application/vnd.in-toto+json
