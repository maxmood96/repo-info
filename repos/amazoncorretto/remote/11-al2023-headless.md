## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:1aafa590663f53ccfeb44e614271b153dfab6c2d5146d0957074e33aad113eee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d9760a74f7405e82ee8e0c3d7faaa6053350fd706f323bacd8fae76abcb17273
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130575253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c931ef9abad608740e579ced7fe8108c1fb2adecc9a14bae2239a8256c2b750`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:16:32 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:16:32 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 22:48:17 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 22:48:17 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 22:48:17 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 22:48:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60449d3418f75690769c347488cf9e42393d2545188b8831ed6941518a568a0d`  
		Last Modified: Mon, 13 Apr 2026 22:48:34 GMT  
		Size: 76.0 MB (76003999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:309cee369e7b5053b89c386bfba213bf5ad18a6f60e3e203fd6318eed59db954
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5212043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c1e72554374bc886132f0d0eb3f4196317c8b22a32116e9b7724dec01a1e3e`

```dockerfile
```

-	Layers:
	-	`sha256:925c602462e1e1ecfe2d761c472d40ca670eb2dffaff2267d781a255b861f493`  
		Last Modified: Mon, 13 Apr 2026 22:48:32 GMT  
		Size: 5.2 MB (5203267 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f15b8b1b45fd8dd1115743e19f41f43f825f8ad001b47345aecbba73afe3ea0c`  
		Last Modified: Mon, 13 Apr 2026 22:48:32 GMT  
		Size: 8.8 KB (8776 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:313664ece873cf7b44d4a8c43314921eee5812ff0abcc29651e1006d9cee2132
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128678281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986b474dafab42d7c798a129c34cac623bc9c8f13035e042456aa19e77b1df6e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 13 Apr 2026 22:21:43 GMT
COPY /rootfs/ / # buildkit
# Mon, 13 Apr 2026 22:21:43 GMT
CMD ["/bin/bash"]
# Mon, 13 Apr 2026 23:11:17 GMT
ARG version=11.0.30.7-1
# Mon, 13 Apr 2026 23:11:17 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 13 Apr 2026 23:11:17 GMT
ENV LANG=C.UTF-8
# Mon, 13 Apr 2026 23:11:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd3575249c042e670ae3a3100192ac7fc74c4cc47ab98f3e4be187916e33273`  
		Last Modified: Mon, 13 Apr 2026 23:11:35 GMT  
		Size: 75.2 MB (75235542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1869b5d26a8b93004430981d3d62272990f7e6a851d4456da46ab29245adef0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5211743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049e2924f20d57cd8cd34f66a92ded5de06482ae2af240829c9eb7bceb642621`

```dockerfile
```

-	Layers:
	-	`sha256:f93f39e6c386f63761840cdb5897e779566bc87d98cd59738f5bbf16823acb12`  
		Last Modified: Mon, 13 Apr 2026 23:11:33 GMT  
		Size: 5.2 MB (5202885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ef78363f28e792a93669ebe82912fec49140c8bb0baa6a517bd3b4518256747`  
		Last Modified: Mon, 13 Apr 2026 23:11:33 GMT  
		Size: 8.9 KB (8858 bytes)  
		MIME: application/vnd.in-toto+json
