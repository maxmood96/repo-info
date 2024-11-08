## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6fae584c6e9f93fa7be51707c15b7c90c71034f42cdf8ababd0838145d9c4d2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:51b5884851f4bcfd77dbced1c0cd456fff44563a02d9b8726c2b2f4e69c911d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141974935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7a44996cfcdbc226318244b28505b70c0f6e90ac6dcbde47402cfc20c7c3410`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:5f3b500dc43eba4cfdf8e70913f712bd20874deac837800a822eb046b9b8bd01`  
		Last Modified: Wed, 06 Nov 2024 19:16:29 GMT  
		Size: 52.3 MB (52344739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e481ab3bd2e1333a817602c3ae7cea9a0bf892a081e2a44b322da92714785ac6`  
		Last Modified: Thu, 07 Nov 2024 21:48:00 GMT  
		Size: 89.6 MB (89630196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d1a29839953c2c88b1be8d4f8331b075ca7f972e430b9268c8bd94d7d7c40fc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:100d1051bee6028e3de18dcffd786a74cefcea2ff23565f3bac711bfa89f6224`

```dockerfile
```

-	Layers:
	-	`sha256:0e2d9c28f76a761681760d128edb4678a59fc0d5057b9a85cefd5b101d75908c`  
		Last Modified: Thu, 07 Nov 2024 21:47:59 GMT  
		Size: 5.2 MB (5211479 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99d117075bb7eeebc3869a090771aaac42ac0b72214b145a42d8ae4e5125383`  
		Last Modified: Thu, 07 Nov 2024 21:47:58 GMT  
		Size: 8.9 KB (8932 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6b0b01a3a9aad65c7def3142a50a6179c48391efa257af42c31612eff63f4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.2 MB (140172302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ef43c3f23eb47eb745e9f2a5004dc4e1274c0dc5f1085efbc180d741bae6d3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 16 Oct 2024 02:18:03 GMT
COPY /rootfs/ / # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
CMD ["/bin/bash"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=21.0.5.11-1
# Wed, 16 Oct 2024 02:18:03 GMT
ARG package_version=1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:ec188ec9ab67d19829a9f75d24a165b6b31e1c611a03fdfabfdf4f1950a2c30a`  
		Last Modified: Wed, 06 Nov 2024 22:31:41 GMT  
		Size: 51.4 MB (51424001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45956c504499f5768532edae726009960deb2e256db0622480983a1ee1fabb34`  
		Last Modified: Thu, 07 Nov 2024 22:06:04 GMT  
		Size: 88.7 MB (88748301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6b3854f93bc09ebb68a77a0c478aa4bca567fc850c97c05193ea9fba38e186fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b1b3c441ceaf645a2422ebc0a3ac53861261940af8add190a732c605f8f7596`

```dockerfile
```

-	Layers:
	-	`sha256:b2d5f887ddf42a488f4f9ac94cfffdfeda530b1407f27f70d036accdd46b7943`  
		Last Modified: Thu, 07 Nov 2024 22:06:02 GMT  
		Size: 5.2 MB (5210270 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:579cb9873da7f4cb5817285ac127f48402c36fca0459fb78fb348ac122469a04`  
		Last Modified: Thu, 07 Nov 2024 22:06:01 GMT  
		Size: 9.0 KB (9012 bytes)  
		MIME: application/vnd.in-toto+json
