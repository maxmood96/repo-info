## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:3865723e05afe0c05df9417d83133bdb0530d7a2ba93629dfc500bd5169128ee
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8d3b496688297ce5acfd42a29dbfe584d94a4a90e5b8a6415f7dd03fc075a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134747752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04506e867593f71a818514e53fcfd5c4e815658efe29beb0f77ce7bdc6a65a92`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:36abe32954e208232b374495838288731226df866aaad9291ccd46166b252416`  
		Last Modified: Wed, 07 Aug 2024 02:04:15 GMT  
		Size: 52.3 MB (52317903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:474f40f82ae783c1b09b5f009a6382ee1b4090fa57ec1480c6a8e20a8e9900cb`  
		Last Modified: Fri, 09 Aug 2024 20:49:55 GMT  
		Size: 82.4 MB (82429849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0781fbcfe5dbbe9f439fd1f1f12bbb51ffe7a58ab86bbd2e333e58b4256e5808
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:842eb7a22ef5539895bb91772dfb8e7a1899f1084386596c7659c84362f5dc06`

```dockerfile
```

-	Layers:
	-	`sha256:aecb9ad814dd83565fff2ec93fbd24a73be689d780e174265a77cd3cba7f9969`  
		Last Modified: Fri, 09 Aug 2024 20:49:53 GMT  
		Size: 5.2 MB (5183639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90d91f45110e76c3ab68686619c8dc835a376ea381e5d00c68480f45dd0c24b0`  
		Last Modified: Fri, 09 Aug 2024 20:49:53 GMT  
		Size: 8.7 KB (8715 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a29f3f21e106f46616426edfe1ed6e0e75e0ffccdff54629ee1adead143a988c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **133.2 MB (133158983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7f9d6b450c3943c6c261009e854b645896e1076135c883be956b2b10af7691`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7-1
# Tue, 16 Jul 2024 22:56:42 GMT
ARG package_version=1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:6dc418e3f016a388470ba66be212f100f862b0633543844e880b17590526cce0`  
		Last Modified: Wed, 07 Aug 2024 03:04:12 GMT  
		Size: 51.4 MB (51409634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1702faead9d8a9992836548fb9353f076f2eaafdb43eb66d56ee1a9a51de8d83`  
		Last Modified: Fri, 09 Aug 2024 20:53:38 GMT  
		Size: 81.7 MB (81749349 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ec59d19b9144f1b6cc926784f77bf406515ce71e29cc5a741a84054fab32feb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7e81b8803ddd054bdc4733aa0c4abd43c7bf3012065c77c96ba6024e0247e8`

```dockerfile
```

-	Layers:
	-	`sha256:5a948446b9dd8e6e6af6b6508704f120067f5f22f5721a81dd0e696a79dac40d`  
		Last Modified: Fri, 09 Aug 2024 20:53:36 GMT  
		Size: 5.2 MB (5182424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f7f4ed081a6499c1b6e3ce21bb642807c55fcd23f4e93a72d68dad1107af402`  
		Last Modified: Fri, 09 Aug 2024 20:53:36 GMT  
		Size: 9.1 KB (9078 bytes)  
		MIME: application/vnd.in-toto+json
