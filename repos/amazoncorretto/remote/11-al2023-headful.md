## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:a419c05a5f0cf78c9046f32e6b16daab66992d254745db9b169fd7be8c2dec6c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8926b8c33d1202e92bdaf420dc01d4d37e4f217eee011e600add31bd18cbbc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.6 MB (130648464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf925d6ffe2db9b22359ec411afff195a5a3c13eef236ab60ac7eed7b75e832`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:05 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:05 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:23:54 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:23:54 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:23:54 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:23:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:1c7de4eb5ced9ea3f72366a34ec955a53e9b0f4ac53d332a155de21eb808d732`  
		Last Modified: Wed, 19 Nov 2025 00:51:12 GMT  
		Size: 54.0 MB (53969021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0498a7f7008be15982848fb0b68a51c0957eac346d7212fa24461cf09bd0a2db`  
		Last Modified: Wed, 03 Dec 2025 20:24:27 GMT  
		Size: 76.7 MB (76679443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d49d902f2b7a019fc71579abff1a05d5506a7a3367abe271845860ad50bf102b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afb4b35b6788f778e47a59e21e0edb0cecfe330404dbb22050c35b457e0bf708`

```dockerfile
```

-	Layers:
	-	`sha256:11eefa767df436978482fa7ef3de20a1205d52371bd82fa58fd15c6b5414f819`  
		Last Modified: Wed, 03 Dec 2025 22:47:52 GMT  
		Size: 5.2 MB (5222244 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f0c3d57ba14960a67ce57c935266ecf9b7b1d7b38971e56c6621f1c4e4451bd`  
		Last Modified: Wed, 03 Dec 2025 22:47:53 GMT  
		Size: 8.7 KB (8745 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:24a3fe65fa1b6600a9c4c95e294bdcab31fae42829b2a3753a3761e0699d1d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128786367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff8449c63796851b6ea775b9f0a5065f1500f1f0e95a0639757fe3c823bc335c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 03 Dec 2025 20:02:22 GMT
COPY /rootfs/ / # buildkit
# Wed, 03 Dec 2025 20:02:22 GMT
CMD ["/bin/bash"]
# Wed, 03 Dec 2025 20:28:21 GMT
ARG version=11.0.29.7-1
# Wed, 03 Dec 2025 20:28:21 GMT
# ARGS: version=11.0.29.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 03 Dec 2025 20:28:21 GMT
ENV LANG=C.UTF-8
# Wed, 03 Dec 2025 20:28:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:225766886c185e8ca1396d025509206d523cf484c336baa393b10b72bebdb69a`  
		Last Modified: Wed, 19 Nov 2025 02:40:04 GMT  
		Size: 52.9 MB (52869421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d8349cb89bccc19573561fc29f9b88476f625d70e57170e7a3bdc72103eaa45`  
		Last Modified: Wed, 03 Dec 2025 20:28:50 GMT  
		Size: 75.9 MB (75916946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:31e12bc2a18c1bc9f52bc6d93e1841fcb0f779f50581e1b8af3ac648788daa01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5230689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8d45a603e022876bbbcaebd4f8f0671fcf483818a98254227bdbaa9ed207be`

```dockerfile
```

-	Layers:
	-	`sha256:f3f00a877984b5aa07be9b68fbc6d190c43a890d99e2a1f5f9d0714df996f910`  
		Last Modified: Wed, 03 Dec 2025 22:47:58 GMT  
		Size: 5.2 MB (5221865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0ddd7f2e39e3ebc6de4fb756b20d10c7025c2ecee074a8710263bb12b9a0277`  
		Last Modified: Wed, 03 Dec 2025 22:47:59 GMT  
		Size: 8.8 KB (8824 bytes)  
		MIME: application/vnd.in-toto+json
