## `amazoncorretto:22-headful`

```console
$ docker pull amazoncorretto@sha256:dd2acc2e3be0fe23fc1a97301a581c04b4f62e64930aad4d98fd4265f2b42268
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c7c8df9efac970ac930baa91f2b924d5cebc0d3c171bb2bf0b6543591bc856be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.4 MB (141361294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c7276b09a1df1a3de3a95261d0e8b2a0c8d57ab2d320a3c2cdbbac63057bd66`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09db8de55fddadefa92f1bae64e21fe9d4ff44377e8833872a549f76e05207f8`  
		Last Modified: Fri, 09 Aug 2024 20:49:43 GMT  
		Size: 89.0 MB (89043391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b7dbea52bcd5c45fe398b98b10f4c8fe70b0e3448095ebc2fd6a06bf640901da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5221555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f52e573f0c61d318f099cb1f83ed5a28ed8a38677c22519270c8d36c629bb821`

```dockerfile
```

-	Layers:
	-	`sha256:bd789621ba6a383b5c2dff6bb30b17c32f9b25a519c26ed815f9ebaa0d13fc78`  
		Last Modified: Fri, 09 Aug 2024 20:49:41 GMT  
		Size: 5.2 MB (5212340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9b1b8db867f270391ea57012fbb16167ba690e0b46f63e7b588ae8c61556fc8e`  
		Last Modified: Fri, 09 Aug 2024 20:49:41 GMT  
		Size: 9.2 KB (9215 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2f363af6678faed595786c3cfcb5bc605535595feb8e09ac3e4defe044e670e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139424080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9eb82e2f993d68325c7bb337b30f437d215b2651970f8a00f073ea53df1646ee`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:660e5ad8318bee312fe2855fcd2ace3debe7a81487d99cc02bd0c4e309dbc398`  
		Last Modified: Thu, 01 Aug 2024 21:25:41 GMT  
		Size: 51.4 MB (51402012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0e62da9c23f6c2bc63e5e53d65284a42bd5bdb7038cd9e7f242023ff4ff0a18`  
		Last Modified: Fri, 02 Aug 2024 05:53:02 GMT  
		Size: 88.0 MB (88022068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e60bfd0aff791e732793aa567a97d71eafca80770586f5a5ae63b9b4da3a0858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5219869 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7d487d50071c5970df7b6e471d5be6335906aaac7fc72e477e3ab788099563f`

```dockerfile
```

-	Layers:
	-	`sha256:8d37fb0056bdce8a04144f83033946bc7ebc0b57863efc09e3a1aeb2051ed307`  
		Last Modified: Fri, 02 Aug 2024 05:53:00 GMT  
		Size: 5.2 MB (5210281 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae6ed6324189ebf47e9eb3f2edfce532fc7fac6125482d0f87fb96a6f1717182`  
		Last Modified: Fri, 02 Aug 2024 05:52:59 GMT  
		Size: 9.6 KB (9588 bytes)  
		MIME: application/vnd.in-toto+json
