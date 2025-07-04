## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:00165d1dfb3a19dff989a1f485078611c5ef12d51d8954636571d2d767d1910c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9c546ffdc03030b38490ef84cd2ce0651fc8143880e6f283648e9c5c6fd13cc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.7 MB (136740904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb041fde3b58eb3cfbffcf989fa1e3c9bffa98f76d56108f9f13042564796c9c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a00db81cfbfcbbcc0cbe194011d1372b5452428d24845777fa6177ed15ce473c`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 53.8 MB (53840211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5151942c3851134156a9337757046fdcec4396522ad35f5d05bffa89c7e2ccc8`  
		Last Modified: Thu, 03 Jul 2025 23:08:14 GMT  
		Size: 82.9 MB (82900693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bef8fb7e6746ee02e020a29858b4f1a88f42554b6e7f2ec0292f2b00035bac04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5217888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8df71ca6fa6dae69397cdf2ec6d6e79f271b95c56a8db516e7914df5ed37eee`

```dockerfile
```

-	Layers:
	-	`sha256:6dd94bc3c9e9126ed01e6158c6d1b33b4c209cc173fa863b6f8da93fedcdb2d8`  
		Last Modified: Fri, 04 Jul 2025 00:48:22 GMT  
		Size: 5.2 MB (5208954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d11a58bd9be4a1e5359749587db3aa74a6dbaeed0cf80e4eb525cfd047bd425`  
		Last Modified: Fri, 04 Jul 2025 00:48:22 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e3788ba321952e213a8139fc873353f6830adb8160567c472a8c0d9236b3e4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.1 MB (135073652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11651a874fc5a4520cbd22c60e20bcb72e55c4150bd643567b2e7e5820ae3238`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=17.0.15.6-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:0e455f237a70326021a937388393d9d7ac6f9ae1616673300f248aeb280add13`  
		Last Modified: Thu, 26 Jun 2025 02:06:50 GMT  
		Size: 52.7 MB (52717557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc429f9dbc62232f087a6d9dba3dbb0be110475b57684271cc4de268129daa7`  
		Last Modified: Fri, 04 Jul 2025 02:56:13 GMT  
		Size: 82.4 MB (82356095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f508e2a58e4ff01bfdf0a2d29da78c488d0def472aa68fd45613a592a0f5ef78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2151b946f37bf842d2a0b214c0d397c7b54b7b29b2628d73e1de3da832450ea`

```dockerfile
```

-	Layers:
	-	`sha256:11bfc188c7ce93215b74af877979ef3d00c05ad3674d294f7fef56b42eb980b7`  
		Last Modified: Fri, 04 Jul 2025 03:48:21 GMT  
		Size: 5.2 MB (5207745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c6b86ec5cfefe2ab684714dcbe55296c3aadc2a090620c2ae2f992dda101867`  
		Last Modified: Fri, 04 Jul 2025 03:48:22 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
