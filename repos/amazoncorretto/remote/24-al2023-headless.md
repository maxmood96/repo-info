## `amazoncorretto:24-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:38e00a37a8d96fa9fc0c7d8ba49ffd0804da2d1d7c9671c67b7d3818309f26cb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3f25c4e550b124af13216bcb2f1b4f802b3bee3a7848252262b4fe5b47118a23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.9 MB (155887595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df466d01782b3aa1b8f995f6df69ccd634ba5868670d817adf28765a2ec247d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:d680ca3f92ab1808f4ae68645f57801d7a408a68d8d17cd7b28da6cfad1ad3d7`  
		Last Modified: Thu, 15 May 2025 19:36:56 GMT  
		Size: 53.6 MB (53614702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a2f9005d70dfa8c4b47d837fe655c5b223b805e149d77af4a486d2aa5ca406`  
		Last Modified: Tue, 20 May 2025 02:07:38 GMT  
		Size: 102.3 MB (102272893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3c2d33689e3728ac652ba5dc48c76146d7c93fad4548f96e27486b7ae4170c0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5201459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de1c97da7850cb032978dc57712fb133c2551ea5cfe25ff7fd0f6d505318140b`

```dockerfile
```

-	Layers:
	-	`sha256:53034a63764801375a29487c43a6ff5472e5807a1fae57fe6951b55aff89c69a`  
		Last Modified: Tue, 20 May 2025 00:50:11 GMT  
		Size: 5.2 MB (5192386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a15202cb158c23175f83f0625e22c4d58a186e9f52fbc5b691c8e00008668a0`  
		Last Modified: Tue, 20 May 2025 00:50:12 GMT  
		Size: 9.1 KB (9073 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:09a7baa9968d84b5d8cda1d8b320c6c995d446347f024ad33d35eca06f06cb28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **153.8 MB (153835861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db54b2e9d5c71bd9a39cea09fefd6719103c8a1f7dcbf29c78671680cb39949`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4f270d4b29a7eeeb2b790617e182170135d4661a5e00a544bb1c992da8525c`  
		Last Modified: Tue, 20 May 2025 00:04:52 GMT  
		Size: 101.3 MB (101270124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a1b958201b1274058ec02beb6a4eca541a648f47a813a46ccb46662f9a56e669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5200362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d46e51d05f9272d949a6ed363730c80dd665809b69b726ac4aa2309706dcd2`

```dockerfile
```

-	Layers:
	-	`sha256:bf42fe3ce77b46b6304a572649180282812634ba136a56e78b582d14e4cb0b1a`  
		Last Modified: Tue, 20 May 2025 00:50:15 GMT  
		Size: 5.2 MB (5191197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2a1691cc87212399c48be51d6732c6daaaea8e392ce14f5a49f88016d479822`  
		Last Modified: Tue, 20 May 2025 00:50:16 GMT  
		Size: 9.2 KB (9165 bytes)  
		MIME: application/vnd.in-toto+json
