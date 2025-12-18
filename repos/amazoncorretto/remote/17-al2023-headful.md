## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:41fda2650ac5498ad992f3e2669d2ec1a1cf5010a82509e737c54ba51ff7719f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f2d0b7911f3875b9945d833045e2df1db2afe40773b8b62d57363b41716d8685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.1 MB (137076422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f50c3de85c5702dccdabc997e9c2f567a83271f886dbfa444a16339bb9cb4300`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:55 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:55 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:18:20 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:18:20 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:18:20 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:18:20 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:18:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8838b07281381e088e59c1c62d90a350301c676e0cf997ca8ee799e0925f778b`  
		Last Modified: Thu, 18 Dec 2025 01:19:00 GMT  
		Size: 83.1 MB (83087962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ab7643d8bacc0cd0755792e94892b37e09c4807cd555dec8fc9888bf45368a4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13f04c4b995c30fc1a74a32ce07dc612f3c1bf46247c4ca1b0f8c59b1bdc8d49`

```dockerfile
```

-	Layers:
	-	`sha256:714dcf78905d350218b6b714596817b3f8ccc0f090fc1733274838f8ed3b3252`  
		Last Modified: Thu, 18 Dec 2025 04:49:13 GMT  
		Size: 5.2 MB (5208327 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65ca470c3e828205356ab1c2b21b2a62fcafa1185c864b9e2db9a3c69ecfca3b`  
		Last Modified: Thu, 18 Dec 2025 04:49:14 GMT  
		Size: 8.9 KB (8892 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f145ed558a8600b68842213120d5ca8b9dd6c56ce6754f710f273e051bdf1f32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.4 MB (135374810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d7b0df5ff25462a16006524be50f494b853b647b7bf034bcc094b98bc6244b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 18 Dec 2025 00:27:05 GMT
COPY /rootfs/ / # buildkit
# Thu, 18 Dec 2025 00:27:05 GMT
CMD ["/bin/bash"]
# Thu, 18 Dec 2025 01:26:26 GMT
ARG version=17.0.17.10-1
# Thu, 18 Dec 2025 01:26:26 GMT
ARG package_version=1
# Thu, 18 Dec 2025 01:26:26 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 18 Dec 2025 01:26:26 GMT
ENV LANG=C.UTF-8
# Thu, 18 Dec 2025 01:26:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f809b08461a497df8a2eccf72e480820907eaa3d47a31f4c24da763026160a4`  
		Last Modified: Thu, 18 Dec 2025 01:26:58 GMT  
		Size: 82.5 MB (82501360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27fbd4233750ff670209a5ca78741b418d823852246390ff4e5c6e8154f4235d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c1168ba656de5ea204a64cfe2563cc00871cea04400df389b2f7f074dacbae0`

```dockerfile
```

-	Layers:
	-	`sha256:3e6a98526fbd72b25a5c49cc444bb0efed64df28666a28fd90a28577cbe612d8`  
		Last Modified: Thu, 18 Dec 2025 04:49:19 GMT  
		Size: 5.2 MB (5207118 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27c75e60fb9241fc9ad90b59dddc10f61db1a939a11f9e18b25e41a1692cbc6f`  
		Last Modified: Thu, 18 Dec 2025 04:49:20 GMT  
		Size: 9.0 KB (8972 bytes)  
		MIME: application/vnd.in-toto+json
