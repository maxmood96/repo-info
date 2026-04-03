## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:b81c0bc3d6183b41e4b64587530c29e71cd6c427983e32835fd3c0266ee94e68
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b6df05f7b4d4a67b758d592b671d42731b13f844ebfe5c6e533009efd26a6da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.7 MB (130739088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4916aed89db5c209516fe1ceb2aa8068f1bf9ee49cae3112289cae62ee711cd7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:02 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:02 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:07:14 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 17:07:14 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:07:14 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:07:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:fd916ef360dd321358d9d165369c9cdd7b0c1f945415eed426c15062374d4d1d`  
		Last Modified: Fri, 06 Mar 2026 18:07:01 GMT  
		Size: 54.0 MB (54033090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:053b060b21607d6be3c2097dd7e946833cf7af7ee6197ca31d856efde55ee5ff`  
		Last Modified: Fri, 03 Apr 2026 17:07:30 GMT  
		Size: 76.7 MB (76705998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:93d7a60f3495e489b90e60dd50f3b11b008173b6968ee95fea217eed9f198c68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f01cdca0100c780496c470ed22e34ce53419db9aba36f8e033b9f757b83615f0`

```dockerfile
```

-	Layers:
	-	`sha256:51f39b8a1e9ad0eb5009889b7af8053f82cc6134f0a4a6bb87ef8cecba45add3`  
		Last Modified: Fri, 03 Apr 2026 17:07:28 GMT  
		Size: 5.2 MB (5222318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1840b29350be8399259cb2bdebc827aff4085c1701fb341121e3ee86680b3e4`  
		Last Modified: Fri, 03 Apr 2026 17:07:28 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4040d883afdfe95c6a39bb2382df6f2075ce44e8e9e0e59086d3117d07422b45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.9 MB (128897774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1105c0870303c63e586344a1f053d9f9301b739d94d63cfc98c08f40de5743b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 11 Mar 2026 18:21:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 11 Mar 2026 18:21:08 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 17:14:37 GMT
ARG version=11.0.30.7-1
# Fri, 03 Apr 2026 17:14:37 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 17:14:37 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 17:14:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:71cb43a93052f17de81c52f47b37a5a2b0f8401a97d4e70aa336f3a87cef4d48`  
		Last Modified: Fri, 06 Mar 2026 20:35:57 GMT  
		Size: 52.9 MB (52941375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faafde6dcd604ec7eec0770c4edd01b1b87be027348be3af0e3e56e6b82c40f9`  
		Last Modified: Fri, 03 Apr 2026 17:14:54 GMT  
		Size: 76.0 MB (75956399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0482f5c71ac4ecbcd3b67f8a7b43cb7a6e629e771461f2196079403ad13183e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230924 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:615c034de525467565ed1c2f1f5cc14d9728243c709d0acd9199bf55ee2756e4`

```dockerfile
```

-	Layers:
	-	`sha256:454650350b06b9e4d4cecacdea5c9b9b71805f4264896483f8f76cb91f3e47b2`  
		Last Modified: Fri, 03 Apr 2026 17:14:53 GMT  
		Size: 5.2 MB (5221939 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcd623ab72a601d500d4334a82fbedfe7bfecdf1ffcc005daa67088ceddd35d9`  
		Last Modified: Fri, 03 Apr 2026 17:14:53 GMT  
		Size: 9.0 KB (8985 bytes)  
		MIME: application/vnd.in-toto+json
