## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:bb59586c2ddda18817ff4bbe78409a515f66c745b3d93040f20c4654563c4702
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:06c750180d7367746f65dff2ea8079de6e58dcbecbf938eab809ce531429db17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131335345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4639c00e1978590a12fe503bbb66e8bd9e25173c992e57e8764ec4f20619e218`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:35 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:35 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:35 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:35 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0490f06cb8837c59d8b0719fd54707fcd9d4482b6277b3016c85ee044dda96a0`  
		Last Modified: Wed, 22 Apr 2026 21:33:53 GMT  
		Size: 76.8 MB (76764091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d85e34fcdeb05e54a81a77af03a15eb2ba1b97200d7aeec142441d669341d325
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151f91f2aac38f12d0b64f8fc30bf41ac57bdad7ede8bb4a1b366a98aed21465`

```dockerfile
```

-	Layers:
	-	`sha256:2a5db73074e67e3a08f9d89ccf874b43fa68bcfb25a77f5b27215cbf38034065`  
		Last Modified: Wed, 22 Apr 2026 21:33:51 GMT  
		Size: 5.2 MB (5228698 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d223aaae33a70af5c04344d50a25189d4ac43c378fdc813dbc8eae19d2ffd1f1`  
		Last Modified: Wed, 22 Apr 2026 21:33:50 GMT  
		Size: 8.9 KB (8907 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3a244dace5547b652a3b49c110ad00660cc33a9c2645fa3f10feb42c102b8bf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.5 MB (129460738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6783714cbfcc0b304e7e25389ad15b69130f9d0cdb1d9b5b941f44de30de0a31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 22 Apr 2026 21:33:30 GMT
ARG version=11.0.31.11-1
# Wed, 22 Apr 2026 21:33:30 GMT
# ARGS: version=11.0.31.11-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 22 Apr 2026 21:33:30 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c9300e29ba701a57389d9fb524b85b451755b02d257198075075485e5e77857`  
		Last Modified: Wed, 22 Apr 2026 21:33:47 GMT  
		Size: 76.0 MB (76017999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9f75b349e8992cfc9195aa16869558f214bc2d33a6e74ad14924713e4179cbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13b9c09def8dc67ade0c347182bb3f58fe0c4e882776959d75b2550b63de5a96`

```dockerfile
```

-	Layers:
	-	`sha256:15b9befb032baa27c0fbb6006fa3e2962a25bdb7c8772efb9f56bad4bd1eea14`  
		Last Modified: Wed, 22 Apr 2026 21:33:45 GMT  
		Size: 5.2 MB (5228319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d783ca3bce3601886e9076f2e1e1f594142a0e02c82f86e5d3ae82916a892e`  
		Last Modified: Wed, 22 Apr 2026 21:33:45 GMT  
		Size: 9.0 KB (8987 bytes)  
		MIME: application/vnd.in-toto+json
