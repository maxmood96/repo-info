## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:ae432eaf629525882276a19967546e5dfcf968442182eb990d6403d8a9f31dbc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d84cdb8930f92c282d48b0b93445b63af64a1bf1e787ed4dbee4481cc7cfd12d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.0 MB (143993489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d85c057ab6a1983c58844222ec42db18c8459a2356162217b3ae83dd3add4fa5`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:46 GMT
ARG version=21.0.9.10-1
# Fri, 31 Oct 2025 00:12:46 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:46 GMT
# ARGS: version=21.0.9.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:46 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390d88380b1c1ee01edfe6fbe8d79c3d2e5056dfe5cc5d3aa28bd5efe2d01887`  
		Last Modified: Fri, 31 Oct 2025 00:13:20 GMT  
		Size: 90.0 MB (89992254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:01f474f5e92ebfddbf74b8dafc1e6ef238e238dd44d72719bdcc7b5e9708c9b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b799feb60d016f55ba4b35519d6d99144fd51b729dc289c0e1e040d3d96be3c`

```dockerfile
```

-	Layers:
	-	`sha256:73a9dc0ff17566a6d4179e4503ac3e3cb7458ad21d9610d9cf632acbb8a57161`  
		Last Modified: Fri, 31 Oct 2025 03:32:40 GMT  
		Size: 5.2 MB (5209943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64d8acefe6fd75cc2f8f4dfb2b9ab6d33116956ea937e22d16899487773509f8`  
		Last Modified: Fri, 31 Oct 2025 03:32:39 GMT  
		Size: 8.9 KB (8888 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6ef664c07975963ea9d970a1cd1b98c0819e2916c9c61e9630a0589673fd3f52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (142032440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41c0d87b12eaf9b6bc2c71f1305f05dcd03aa9733de04d9905a50905b975a281`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:14:56 GMT
ARG version=21.0.9.11-1
# Tue, 04 Nov 2025 23:14:56 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:14:56 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:14:56 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:14:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a232e87776271ab2f683e5140e8aae8f799a2e16e5eb0d3bb696207fd7442204`  
		Last Modified: Tue, 04 Nov 2025 23:15:34 GMT  
		Size: 89.1 MB (89130589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dad2e1eb28120a9f7db6e282dde7476b28302010cfcaee964cf077a871d96d3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:662c84d984bc7e315b07964be757fab802ad9ddd55c81f9fdd40bd7bea25a9d2`

```dockerfile
```

-	Layers:
	-	`sha256:432461c7877f2f280d3d142107c2770f456aa42639f5440c21fd3be0643a3bde`  
		Last Modified: Wed, 05 Nov 2025 01:48:20 GMT  
		Size: 5.2 MB (5208736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e7641cfa183a7f93cbcbff0f951fca85ed8117cf644980d59b00c7f31703780`  
		Last Modified: Wed, 05 Nov 2025 01:48:21 GMT  
		Size: 9.0 KB (8969 bytes)  
		MIME: application/vnd.in-toto+json
