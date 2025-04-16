## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:fd6dcfd2efd07b6ac87513a40b1eec3e97f895ad675039479e243ac1606a6a47
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0968f62c1f88d9ac34b0e9b600d0b2985bd8da76723d2a2df3f4daeb68350d57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.9 MB (132928889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b8a0bf1163ec51b34bd79f498f0785f0c58dad380a6b17ecc507124bbe7a860`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:23 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:23 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3425fd24c704acc2d09abeaa5eb7a49cdb5f4220666a43452a9dd65b0f481c`  
		Last Modified: Wed, 16 Apr 2025 00:08:43 GMT  
		Size: 77.0 MB (77021836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:10955358ad6f18228842938bfbac8ffb267f34aa02def4cd0f459c06217bf365
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f66c084c893c3381ff6cb50ee7421c313ad2b596eacd2dd89a7bfa67f5333f`

```dockerfile
```

-	Layers:
	-	`sha256:3b6c747b48f046504db520a0112fe85d4562aa8bc80b518364626d4800b207b7`  
		Last Modified: Wed, 16 Apr 2025 00:08:41 GMT  
		Size: 5.5 MB (5464951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98c246a555d5567b141250a2f699e650dfdb9cdeda7ec04a4eb39b48ebc9e5e`  
		Last Modified: Wed, 16 Apr 2025 00:08:41 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c29453216c38f58a92707f492b59d23597d0b6397cd166142df639dcec093b6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.2 MB (131204716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18b84667d31e4d14016669200eba8a7826c95c8ba825bdda08e2bbc5ce81e6f1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:28 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:28 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2607cd4c0e32f00e7a4e2a2d91efbfb9cc75ec102edd25deae66333016c0507d`  
		Last Modified: Wed, 16 Apr 2025 00:03:31 GMT  
		Size: 76.2 MB (76243707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b26226278cbd2f8d88cafbaf2ed722c75abf4d4abad5ed27ce69f9c29f0d49c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5473439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdc6e492875dcb5444731ddf00d3179a569bc31b8f7fd3be7bf039685bad3641`

```dockerfile
```

-	Layers:
	-	`sha256:6adf93209a493f6e4e9d3479e2e2b9436abda3398d341ad5ef241c32942f9825`  
		Last Modified: Wed, 16 Apr 2025 00:03:29 GMT  
		Size: 5.5 MB (5464572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1455c2742f52b2ed147be77afb021eb6a973b32ef373379c29d0239634a17709`  
		Last Modified: Wed, 16 Apr 2025 00:03:29 GMT  
		Size: 8.9 KB (8867 bytes)  
		MIME: application/vnd.in-toto+json
