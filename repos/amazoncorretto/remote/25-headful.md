## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:a93ea3e82cd89e9583929847a0b248d4b83d30e8a92da743ddf141a4f36c0889
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7de9626a4d75e0b2804f1108c8fd1a33b3d0e2ff4b35567d692c356f14849f77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158331719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20db6cf83cba90011582f960183853dbe80f1336bdcd2cee867e494ebc912d62`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Wed, 05 Nov 2025 01:07:16 GMT
ARG version=25.0.1.9-1
# Wed, 05 Nov 2025 01:07:16 GMT
ARG package_version=1
# Wed, 05 Nov 2025 01:07:16 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 05 Nov 2025 01:07:16 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f5cfb96cbe81038e62e33b83f3a67eb5bcdbc4290829c4ef66a8f4b861dec4`  
		Last Modified: Wed, 05 Nov 2025 01:07:51 GMT  
		Size: 104.3 MB (104330484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6739ec2ef952430cdf9000a00b96aaec359bb0bb4663ea639127115e0096009c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a5d21bf336b7ab5da8c4aac340337186e6363f3be4f0dde95db6c83016d8925`

```dockerfile
```

-	Layers:
	-	`sha256:8fbc44a04d30cae0d5769dbac63fe5e3b4f04a519afcc7e33ff58ed862185b0b`  
		Last Modified: Wed, 05 Nov 2025 04:49:31 GMT  
		Size: 5.2 MB (5220208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc9e5f083013f7fcfd01d7b42357269b6a63f2ef89bb1009bd29b6a0e61f09d1`  
		Last Modified: Wed, 05 Nov 2025 04:49:31 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2ecff325efcb978c1b1dc949295d3247775da7ef9ac593b2a8542455449eafdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156178667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780391fc586064c59301822e910ecfb059b5b5dac43a5970d718f0a67368a394`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:16:42 GMT
ARG version=25.0.1.9-1
# Tue, 04 Nov 2025 23:16:42 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:16:42 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:16:42 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85afa25beac1d0bc306619ce763a649516bf26a0c575f81cef3ef50a9ee11b`  
		Last Modified: Tue, 04 Nov 2025 23:17:23 GMT  
		Size: 103.3 MB (103276816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d2831526209a9fd1fe35151dd704feda3f30145cbdf05112d108152b5e68b673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2804f6a32d7b37dce5eae9bae25f14923cc568ce448463b8e9314da2110871`

```dockerfile
```

-	Layers:
	-	`sha256:1d6a7e26cff85b8540888c4aae20f5fcd54211ebce3e891c520bc2c66fb2da0b`  
		Last Modified: Wed, 05 Nov 2025 01:49:43 GMT  
		Size: 5.2 MB (5219022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317426b955a95c5e2b7233313132c210620d1d140bbadc07ce8ebd61059180a5`  
		Last Modified: Wed, 05 Nov 2025 01:49:44 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json
