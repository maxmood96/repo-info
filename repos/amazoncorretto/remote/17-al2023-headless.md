## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:8555d2b6d8547b4ab2eb5244931363d0d8f5554adf0e86853c20e2efb27b9bdc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:de773be460c13951d9fdf5dec55c96dee9e1ec3ab5239a0db3344ce6cda6bb6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.3 MB (135270096 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73c1ac5524b7b8be6669644b09c48af1e75234e98e1d8d6977e7b768007bb37f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99f84128d778e956fddb954bbe0f89122cdfedee57e71adf038440ac68cdd7e2`  
		Last Modified: Sat, 11 Jan 2025 02:29:26 GMT  
		Size: 82.1 MB (82119621 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:315672c3165a8a1b6673466b61720b9b0bca7519eb71f6e7b55b5f531bfe6928
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d052c59970b5ed03e88432092f4bd7950b034248d1853a319918204c7f91e9e7`

```dockerfile
```

-	Layers:
	-	`sha256:cf3835b5d3d1b9d408aca8f49596a6ddfb248379b0e35260c7a405a6f84a40ea`  
		Last Modified: Sat, 11 Jan 2025 02:29:25 GMT  
		Size: 5.2 MB (5179424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07aabea1f74cc67ba3bdf79e64f69590b5ecf9f4d35cfdd52ad4ee643e1cdc16`  
		Last Modified: Sat, 11 Jan 2025 02:29:25 GMT  
		Size: 8.8 KB (8756 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5390f1ec6e850e04ea7f3066cd5b6bfaefb944dad1285d40f5b48ef5aa6b4371
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.8 MB (133820697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a64df90e4ee57eaacf093104c779e4a8af7251e3e91d79def4dac9a15272f7bb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa648fb98008242e99579dcbc64cdcb850bd0c78c767341ae22dd6b196fce6d7`  
		Last Modified: Thu, 23 Jan 2025 18:43:34 GMT  
		Size: 81.6 MB (81552501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73dae44fea6a060aa416ab5505e9b94df2d19550fab3d5412b3eeaae55a29d7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5187038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ad838e5353c6cf1275fd71ec0ea0d4232cef391af3a3fc3f36c01f5946cdffe`

```dockerfile
```

-	Layers:
	-	`sha256:e8661036dae8f499a9bc7cdfd299d6442a8e5346f4f5366d2d7b8b048fc1f76a`  
		Last Modified: Thu, 23 Jan 2025 18:43:32 GMT  
		Size: 5.2 MB (5178208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90499e02b073da5c1ce26d748fb1b79e55cc7d6c2454b9782dc083e8f47a1126`  
		Last Modified: Thu, 23 Jan 2025 18:43:31 GMT  
		Size: 8.8 KB (8830 bytes)  
		MIME: application/vnd.in-toto+json
