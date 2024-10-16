## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:646a090207b8cab40aa5cbb5d670aed8bc324f20e600ed2aae8c2e9c955f8771
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fd224ef39b583d2e6ec0e369489d9f01c714e72afa36509f6eb3e798a52bb364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135100506 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde8e0dcf8d2539a506a4d68e9be8370733989e623972b30b567cefdbc5ec061`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:49 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:49 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5acaf245b9570e79c1a7ee03a5dbc0f7b4aa375f3354879d41247976f76d0c4b`  
		Last Modified: Thu, 03 Oct 2024 20:23:24 GMT  
		Size: 52.3 MB (52325305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2beeebb2cf3af53266c681c5d1ef41810af785d0935f22207a4d65612d15e30f`  
		Last Modified: Wed, 16 Oct 2024 17:57:49 GMT  
		Size: 82.8 MB (82775201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:094e12fd49ec6b67a30a3756c4cf9faad32305b6b85046fd5bae51abcfb42b4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f191c3a45d46b99cf251936b54d220fe2721daafda55a705696a0441bf316b0b`

```dockerfile
```

-	Layers:
	-	`sha256:dbe5464e2914ba957be55d1435448dde6320155f0dc243d22152027d9be4dad3`  
		Last Modified: Wed, 16 Oct 2024 17:57:47 GMT  
		Size: 5.2 MB (5209691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42a8b7bd9aff9ec6b7b7428a6225735281fb8f31f7fb57f28db60a538574a66f`  
		Last Modified: Wed, 16 Oct 2024 17:57:46 GMT  
		Size: 8.9 KB (8938 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8790de5d27968593afcca22be11b5fa48f2bc8d4d16527bd5794221e56b80b31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.6 MB (133568453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61592713d853ee5fcbf2382993f2afb1829a6c066198e2aabe0c4e34c8a4b6df`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 03 Oct 2024 16:34:52 GMT
COPY /rootfs/ / # buildkit
# Thu, 03 Oct 2024 16:34:52 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9e91bc818827f819b6de2c247e4fed5f971ec9990bc2b6330e067ca2f956815d`  
		Last Modified: Thu, 03 Oct 2024 17:46:58 GMT  
		Size: 51.4 MB (51426364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c498b0de3313c3512e3f20f7be59766ded6cb7cbc0854981c39c64be03e92c`  
		Last Modified: Wed, 16 Oct 2024 18:23:18 GMT  
		Size: 82.1 MB (82142089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:239da7401d3cbd026529fe3076b9c47895cbf63efd63fd76e6627325c48b6008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a171c7f2fd263a07fda6d53166f83329220d0caac9c66db314043220da9fca27`

```dockerfile
```

-	Layers:
	-	`sha256:649c5e5b693e84329976efd466f822e30e5816c8e1fae972b1ac1c90de4166c3`  
		Last Modified: Wed, 16 Oct 2024 18:23:15 GMT  
		Size: 5.2 MB (5208480 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2df07bbe7d37a7d2ddc973026902b5d1c082652335b90dc3326fda4b8ef5a74b`  
		Last Modified: Wed, 16 Oct 2024 18:23:15 GMT  
		Size: 9.0 KB (9019 bytes)  
		MIME: application/vnd.in-toto+json
