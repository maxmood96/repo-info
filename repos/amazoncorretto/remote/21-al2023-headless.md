## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:37f9f1564cfdd12066fd31e9caecc800ad164fc287abdaa4b4b064393abe7d30
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3f63448dadb8956f42b14e1aa2e7c405bd7678abd5a985deda4a35cb437ecad8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.9 MB (141910567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c8e9f7ea1bfc6222dce55d0e477c84b1bfbb930591da896a497b991acc3716`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:50 GMT
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
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f122d614e3d5efd382b625becd9a9945f9dcf3ac6cd04d51a26542a9d08aa43a`  
		Last Modified: Tue, 24 Sep 2024 01:57:56 GMT  
		Size: 89.6 MB (89585609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6e99779c7007aa39a7e89b3654ce7a87f712baee675c2938ee4ecc47a6fabdcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 KB (8495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbda82429740b2cc64b6bd57d1013e18be9399afe4eed29b8cdd059878e6d4ff`

```dockerfile
```

-	Layers:
	-	`sha256:27a36d3cf0b8f438cbd8dc6f8c9fc05fd1a80e07477bb127a4c8084581331605`  
		Last Modified: Tue, 24 Sep 2024 01:57:53 GMT  
		Size: 8.5 KB (8495 bytes)  
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
