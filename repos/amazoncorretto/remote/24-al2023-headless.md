## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:b701d42c766b6c52e89d4228e460beebc05ce8eeddc2196a7447da1e5b5c0ad1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c62589889ab2800a64d03a6f7e96b89e20535986505114c40006a95adc693d50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.4 MB (156446838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47e8dc035bd3e266cc37310b035c1cb209712a5015e4db55a9e0fc6cea06c01f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:fbd59a98b07e2495a3d310a602c2cfb73ec51acb403ff01759389020a766d513`  
		Last Modified: Wed, 01 Oct 2025 20:54:00 GMT  
		Size: 54.0 MB (54005131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34d858761e5bb8560c2dc142bd2da8c37dadf7125864bb7404b264256dd45f1`  
		Last Modified: Mon, 06 Oct 2025 21:14:10 GMT  
		Size: 102.4 MB (102441707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:383248d35e14f82d6142fd1b986c53ecfc500ca10e349251f712fe590c6d2e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:230e6557cf30b0cbb2104a33c56171a7ece6440eb691bad275636a328d945cd6`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ac0423c8022722b1edb36784ab0bc649d98fc51325a2eaa80bef28401e446`  
		Last Modified: Tue, 07 Oct 2025 00:51:06 GMT  
		Size: 5.2 MB (5194701 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5825bc864012669743dcba7a0b22d798a7a3c89395f8ce19d0370a851050998`  
		Last Modified: Tue, 07 Oct 2025 00:51:07 GMT  
		Size: 9.1 KB (9074 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:269089912d7d209a21f492199d2a6a3a82007cea2166dda08e8bde1eb718e5e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.3 MB (154346586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3437918812fd5b42ba5bca2414696b5123a10f01a56633c5685087bdeca3675`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:d20954a43d82da3800edf6dd0aed422de3c1214f01f7bc8f0cb120ccc89c5d00`  
		Last Modified: Thu, 02 Oct 2025 00:57:55 GMT  
		Size: 52.9 MB (52891203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba56d7da99342d8c89c9784a37af44447b80e6bd7a7a681cb74fb5b348df9a7`  
		Last Modified: Mon, 06 Oct 2025 21:14:31 GMT  
		Size: 101.5 MB (101455383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47a9806977fbf2c210b4d5adc7b56f10e27a1a66722dd97d5b7e0af9aab4762a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b28d8912ce8f675aab47664d985f7c9331e0392323d1da0bfa06cc9d21ad075b`

```dockerfile
```

-	Layers:
	-	`sha256:a7eec418a2c168e15c724f6826db45c0c5ac7b9bfee5122f942167ae080433af`  
		Last Modified: Tue, 07 Oct 2025 00:51:11 GMT  
		Size: 5.2 MB (5193512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a03e21b3a27e7c11550657e5bd3ee0a58b726ca7a0aabdf6abb7f0c4458ca118`  
		Last Modified: Tue, 07 Oct 2025 00:51:12 GMT  
		Size: 9.2 KB (9166 bytes)  
		MIME: application/vnd.in-toto+json
