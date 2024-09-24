## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:d2a4c9c079c21ee5db0052a1179a1901ab6e76283dcf1b62a280cd9486a0b4b1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:87ede0d3b599bd49278d5dfb77622c2edca7084825d7cb9f950f584f31a04ade
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.5 MB (128481470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b59c971c5ea5d2a722f04d55f036e010cf46dd7df086d28f33a6417f9f1d4b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:50 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:50 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:9a0f8ca95549caa504c79acef976bd6b204271a0f61eacfa1a045c2ce6bb0d43`  
		Last Modified: Tue, 17 Sep 2024 02:04:40 GMT  
		Size: 52.3 MB (52324958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8952a0c3d13371951687fa939412a9c456172e1f9bc020e6292a8a26e2ecb883`  
		Last Modified: Tue, 24 Sep 2024 01:56:41 GMT  
		Size: 76.2 MB (76156512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5009a093d190c3adec0ae97a1121eb7b200bb7117b91ef6ac5d95ee13eb4e326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f78f413a8daf89316469bd5d0b4146d223947851ad5a1de55c63a18deaa4a73`

```dockerfile
```

-	Layers:
	-	`sha256:c0df8cf722c47166912a0cd4d38502618ea0f0e7c37d9cf64e77ef46696f9fde`  
		Last Modified: Tue, 24 Sep 2024 01:56:40 GMT  
		Size: 8.4 KB (8399 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ce7da35a57bf32082fa478b3ef138e08cf2c968566665be67c97c1f024bb16fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **126.7 MB (126723848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9d2d7541030f46b172948dd68dc7df2628f864db2014f5b0fe81f2dddf3d9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 16 Sep 2024 21:25:53 GMT
COPY /rootfs/ / # buildkit
# Mon, 16 Sep 2024 21:25:53 GMT
CMD ["/bin/bash"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=11.0.24.8-1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:8e0a984b7f222102e6d0bbaa2dac67ec2c00d5735727c1b5e918160055b8f617`  
		Last Modified: Tue, 17 Sep 2024 02:35:27 GMT  
		Size: 51.4 MB (51425992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dee73b0fe878143ef9ef7c6bc8dd6b81855320d7806c594a1ef0c9f973c7883`  
		Last Modified: Tue, 24 Sep 2024 02:31:39 GMT  
		Size: 75.3 MB (75297856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d07b33481853c174c2698cc76db1b0d40e77d3a303c1caf5e3f73beec3788e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5207095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2157d6b97c9f06893794b6434e0f0fbda5d30e7db89bdb4a283d6c1a5e21bd5d`

```dockerfile
```

-	Layers:
	-	`sha256:280c70c2baf9eec2db013e76f8ba388521726e6c5c760d2b84b16f4b0adde7cb`  
		Last Modified: Tue, 24 Sep 2024 02:31:37 GMT  
		Size: 5.2 MB (5198116 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bd8831ed77f7ad3bfbd277f8e9266342fd387cdc63878401cf508a1d7555627`  
		Last Modified: Tue, 24 Sep 2024 02:31:37 GMT  
		Size: 9.0 KB (8979 bytes)  
		MIME: application/vnd.in-toto+json
