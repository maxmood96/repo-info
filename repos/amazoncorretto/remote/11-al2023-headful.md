## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:e2500e447a651023ea9406488a4568c26e25deb2834a1978decd8ae65c6c1d37
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:342197a70f4ae119a0ffaf21200e61c49d65e50fdc7be7444151b15ccb084bf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.1 MB (130075000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc87e2b9b75991e62cc2093bb6966738e5102b633f4991080e753941d103fbf`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=11.0.25.9-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=11.0.25.9-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80730a78c02e7159164cfdd9ae2d91a8e6d0a21d3e185160542366050e8fcdf5`  
		Last Modified: Sat, 11 Jan 2025 02:29:18 GMT  
		Size: 76.9 MB (76924525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48b2e4b7be28e8de0ba91e680e7e6a97ce6dd9c0b10b9232d6e67d4fa2336404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057531168e43577c5c1295b75e9f61b37283f33bac5f363549408e16b8f72eb8`

```dockerfile
```

-	Layers:
	-	`sha256:7baab73fa0dce9e56ae306406a259e21af648d77e7dbd23c2188b46873e23b11`  
		Last Modified: Sat, 11 Jan 2025 02:29:17 GMT  
		Size: 5.2 MB (5218593 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0b2bbe00b09ded2d3512a3b6346c73750ded9b41137dbb01e55a0969632ee5d8`  
		Last Modified: Sat, 11 Jan 2025 02:29:17 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b3b8b12749c5cbb45684ba37839b7e297c90a982ef11385cdfa0aefe09a9069c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.4 MB (128395904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8784f8db9386310aef14983e7ec82f23d59c45811867723b5b5568c2f486e261`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1962cb6da6d19ba1251c442b2ef5ae9d2a1e1b337388c393fae1d87f184022c9`  
		Last Modified: Thu, 23 Jan 2025 18:37:11 GMT  
		Size: 76.1 MB (76127708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:60de3ed2136170f9c7b6ad2a16476006c67172aeab7b8db4dcd10b3e167ada4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5227082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143af5338c719f09e93a09aaba9e62043df1c08662258924b31cf97c5ae690c2`

```dockerfile
```

-	Layers:
	-	`sha256:bfcaaddda937de8a885d57224e9c469fb9eceb1dff72cb47b99e0c27e1307179`  
		Last Modified: Thu, 23 Jan 2025 18:37:09 GMT  
		Size: 5.2 MB (5218214 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f18894ead366a6092cc64294cb9c75ecbeef808b8cde7c91e2d825290df90fba`  
		Last Modified: Thu, 23 Jan 2025 18:37:09 GMT  
		Size: 8.9 KB (8868 bytes)  
		MIME: application/vnd.in-toto+json
