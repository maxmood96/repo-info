## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:2e5beef57b3974bf7c083f9771389324a59e0f1aeebd27196da380b1fa695225
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:537e73a03ca8fabb9b6e6fa5a359db82a92a1f7e2aa8db3765faf2614a2ed92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.9 MB (143949236 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40ccbca7aa4375852d411e69ff71b48d42a1060834c4a50aff100fbcd519d86a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:46:09 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:46:09 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:13:12 GMT
ARG version=21.0.9.11-1
# Thu, 11 Dec 2025 22:13:12 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:13:12 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:13:12 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:13:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f0d8a57b0a961dc24c52321274c89319998d2371a5c75edf34df5d320f6cc484`  
		Last Modified: Tue, 09 Dec 2025 04:05:55 GMT  
		Size: 54.0 MB (53988460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e492bb1ad2c98f5bec19ba1b69bc4fb19338334ded64975a97523946d2b69f8b`  
		Last Modified: Thu, 11 Dec 2025 22:13:44 GMT  
		Size: 90.0 MB (89960776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aa5c1452b247b27a8efb67dc66613517d7c6904fed424aedaa581b5a71593d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5218832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b1edc1fb17eb8372d4d4a64c7acb4f64ae6503707f1cbeb40e00f9ab44f619a`

```dockerfile
```

-	Layers:
	-	`sha256:e46605e0f28a948412366934065330ac2c50dffd65d397811a89a7412eac45c9`  
		Last Modified: Thu, 11 Dec 2025 22:50:13 GMT  
		Size: 5.2 MB (5209943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1353aa4bd1d8db5396f002fc274bb2f00ccca2a3385a4e6b7c648051318bd131`  
		Last Modified: Thu, 11 Dec 2025 22:50:14 GMT  
		Size: 8.9 KB (8889 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8d5195e78f4d4f2d3028b26d8e69b88be450510ae2722263911585e1bdaba7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.0 MB (141970676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc466f49357873cfb9662bad047dd6def1cc935312e05a8a96db9248cb2af31c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 11 Dec 2025 21:45:58 GMT
COPY /rootfs/ / # buildkit
# Thu, 11 Dec 2025 21:45:58 GMT
CMD ["/bin/bash"]
# Thu, 11 Dec 2025 22:12:44 GMT
ARG version=21.0.9.11-1
# Thu, 11 Dec 2025 22:12:44 GMT
ARG package_version=1
# Thu, 11 Dec 2025 22:12:44 GMT
# ARGS: version=21.0.9.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 11 Dec 2025 22:12:44 GMT
ENV LANG=C.UTF-8
# Thu, 11 Dec 2025 22:12:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2de128a65b40f541240900d3ef927c69205504fb73b977065e0eaa128c1e3777`  
		Last Modified: Tue, 09 Dec 2025 08:35:33 GMT  
		Size: 52.9 MB (52873450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74b7bc46befda8c50ec65292f11ccf7a5a27f55156ef4a1bd1cf281c0319bda`  
		Last Modified: Thu, 11 Dec 2025 22:13:18 GMT  
		Size: 89.1 MB (89097226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4b5409a2af676b0c29035830a5a206c6c1c11e107c24feeedc108ec63781a359
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7b19096d1e250ba85d77dd8c665c7a46f7fd2d4bf42676724f9616f2372426`

```dockerfile
```

-	Layers:
	-	`sha256:867d2601583a271063660cff9ff454791608881e1160c4438bc03b3a55b75fcf`  
		Last Modified: Thu, 11 Dec 2025 22:50:20 GMT  
		Size: 5.2 MB (5208736 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20191fe2417b3f4525a707684c95778796539cdb658451e58614afb39ceb957d`  
		Last Modified: Thu, 11 Dec 2025 22:50:21 GMT  
		Size: 9.0 KB (8969 bytes)  
		MIME: application/vnd.in-toto+json
