## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:8c4091cd56108fccbe43b2e3d3a7b7152eff38f58315f4e45007099a76bba0cd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bea6fa95c775ccb955e4058930d77a0fc2620f16d1e227298c72ffebe306b219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.5 MB (130521514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc3beaf7429024467172802d9005120836fc84917d758a51e3620ca142e2b33d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ce6eef9359bdd478ffb7f92bad631b8687e6b8a01095407f5e645e0d541bbad`  
		Last Modified: Fri, 13 Jun 2025 17:03:28 GMT  
		Size: 77.0 MB (76951154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7de4bb9d40f416e27b16458a46a2d7f4291c5b6f2d5c97c679ba4258f7525c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5231659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:156d4aae41335d3549c796dd291ab88c9d61d5f099069929931714c2dfa370c2`

```dockerfile
```

-	Layers:
	-	`sha256:daff224e062cb9adfb7cf7bb7f4dfb089167d3805382fb1ba59a149239702039`  
		Last Modified: Fri, 13 Jun 2025 17:03:02 GMT  
		Size: 5.2 MB (5222871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e238ca3658aff5c9da7e0dd9e564b887afd44f48bbc64a3a532b469164c1dbd`  
		Last Modified: Fri, 13 Jun 2025 18:47:37 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:33416be31dfe798a9e30fe8771ae820c787afde6098206011aad2d42694d1e86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.7 MB (128729294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a253e16949c2d6b263d467b3a1f62b5b5ea69ce885e420737413858fbd57969`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=11.0.27.6-1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e31bf93b5ec13a736d81e6380f6083f033d564e67ad32adafc2bda8e1d83f25`  
		Last Modified: Mon, 19 May 2025 23:53:01 GMT  
		Size: 76.2 MB (76163557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:53b0cda945b3ba39c5420698544c00b359f53bc00cdeb17857890aea984ffd62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30e802e37dcbdf06abb7dbca98bf9d403f7bde3ced81340cfc04ddac57c36036`

```dockerfile
```

-	Layers:
	-	`sha256:382876e5ac9cae11dad3033f10533eff8632d7912076006942d64f9558505e51`  
		Last Modified: Tue, 20 May 2025 00:47:51 GMT  
		Size: 5.2 MB (5219478 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3cc7e6e7380e397cdc991aa58707d4cb43aaa8c350b9e1951e5f59560a6e9438`  
		Last Modified: Tue, 20 May 2025 00:47:51 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
