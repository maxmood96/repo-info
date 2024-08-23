## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:4f2c1dd584010b71003cfab117274a9e725014912e25ee4fd3a77a5795bbcb00
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-al2023-headful` - linux; amd64

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

### `amazoncorretto:22-al2023-headful` - unknown; unknown

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

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fc78bd69fea592adf35b0dda934362f38398c8f2d766e321501f58da5458c292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.4 MB (139434891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1efc53f9aac7f1477c554811e36ee33170a70700603ba723f8d78679afcefc61`
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
	-	`sha256:875f26d62c6d0f5a935b0c8548e8375f2a9b98d7669bf434dcd5b36e2114348a`  
		Last Modified: Tue, 20 Aug 2024 01:54:55 GMT  
		Size: 51.4 MB (51426298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99883c38a46bc138b36a157327041bfa52f6fdf7231acccce240eb91ca6a8a74`  
		Last Modified: Fri, 23 Aug 2024 02:38:51 GMT  
		Size: 88.0 MB (88008593 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1c6d8218e41d10bc87bee0f0b5f30edda6ad6ff5f1fb7559b6335016e6b0b3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5220003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e165f57d45849793497c7c4fc39f7166bf28880a48d3c6ba6f6a5c2dbc260ccc`

```dockerfile
```

-	Layers:
	-	`sha256:fb4a2dece0df2fa672216bc06f3d4aaa6da50ffd08b7280e98bf3ed7b7ea70cd`  
		Last Modified: Fri, 23 Aug 2024 02:38:49 GMT  
		Size: 5.2 MB (5210415 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bddba39ecc28efc9866d7b17e3237b586e97132cb0c37de5247592bf92b3682f`  
		Last Modified: Fri, 23 Aug 2024 02:38:49 GMT  
		Size: 9.6 KB (9588 bytes)  
		MIME: application/vnd.in-toto+json
