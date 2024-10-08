## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:40d940b64efe98e42a74780d74c303087a080024e73e86afb5b16e97ed50991d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8fcdb0ac2aeee265d34be931a27564cd5d003667efdef5302d54c6b80d63df78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141911127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6d1481ad8703e7f543c316690b6cce184c514e797126cdc5d3ebcb0d77d248`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 19 Sep 2024 23:46:25 GMT
COPY /rootfs/ / # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36b914ac439ee3c5922c0bfb3b72e04efb865ad80e79d0bcacbdf3129c628c26`  
		Last Modified: Tue, 08 Oct 2024 00:01:00 GMT  
		Size: 89.6 MB (89585822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:663743128d345cb1c876eddda499a51b79fdb7c704c69efcd8f0d571a3e58aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af1c5e1a3ce29e659ba959163832ab3ab407e23be5fc70d6258717e519e5099`

```dockerfile
```

-	Layers:
	-	`sha256:61eb712c5b3ab4042c22efcf9b9f9a974a392904adacfe376a7819682f95c056`  
		Last Modified: Tue, 08 Oct 2024 00:00:59 GMT  
		Size: 5.2 MB (5186188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:31e1e8a0cc97ab935683928bcd2ea3c352d4cef8d5ad101c3a6e7a1298f41f7e`  
		Last Modified: Tue, 08 Oct 2024 00:00:59 GMT  
		Size: 8.7 KB (8718 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6134dda11d36e324f9922c1685589706f75d7ff81c5a1ab1ed32786099af99c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (140037278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6d55171383f5609cc43630c8b47fdf332302848482490ec0c720a4cbb780ff8`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=21.0.4.7-1
# Thu, 19 Sep 2024 23:46:25 GMT
ARG package_version=1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=21.0.4.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e53e0158fa032928c8c48a8acb688ada1bc3ffc76711754224949e68c06d73`  
		Last Modified: Tue, 24 Sep 2024 02:44:33 GMT  
		Size: 88.6 MB (88611286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:557edb018e16ab0fc65c3ad0817b312a468550f6af229e78a08c6c78d69f3793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5194038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aab9d9e48c8b0b2846bb91d080bb5d26a4bc6033460669681d85d7d8ce81859`

```dockerfile
```

-	Layers:
	-	`sha256:31010c0e36f7d2a27029cce068d6b676ac039f1f36b288c18f74048d4454b77f`  
		Last Modified: Tue, 24 Sep 2024 02:44:31 GMT  
		Size: 5.2 MB (5184963 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8eb7c40489d172f96ef64fba6a63e875dabb19e9d27af622d989a98e9bfe6cfe`  
		Last Modified: Tue, 24 Sep 2024 02:44:30 GMT  
		Size: 9.1 KB (9075 bytes)  
		MIME: application/vnd.in-toto+json
