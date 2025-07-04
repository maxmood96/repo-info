## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:344932704758a73a35885c5863dd7f27bee08d180d8c30e84c8c2e310696a1b6
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
$ docker pull amazoncorretto@sha256:e56b1efc001af4af102ea1c3f83b014e7a587832263c7982b5615d764087c7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.8 MB (134836904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6695d7cc9f30adf72427ab90d644e09a47d706ce8707144c14132c0f76595bf6`
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
	-	`sha256:2913b957e7cca1539a6d274307081564a7142eae485bcd51683bbef9106592aa`  
		Last Modified: Thu, 12 Jun 2025 03:47:32 GMT  
		Size: 52.5 MB (52481692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4c3dd6ce56d5be5db670212cc3cefe6208e2e0669f15ef455679168cfa56ec`  
		Last Modified: Sat, 14 Jun 2025 00:02:38 GMT  
		Size: 82.4 MB (82355212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:11956bc80cf6ad67643973d479821a1b62123bcf529cb52084dd687bb4cc68ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5216752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4a0dc9377c1244eabf11199f664b06ed256c0f47677a9bf8344ba0ca42422f`

```dockerfile
```

-	Layers:
	-	`sha256:863ec018bc4ad8542e94fb4456a6e67f0bf0e17105281d1a49b58ce90f0aabab`  
		Last Modified: Fri, 13 Jun 2025 21:48:19 GMT  
		Size: 5.2 MB (5207739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e52c4d348c0a2f9186fe45268348e8e42c5498328ddf5a72e1af72181bc772c`  
		Last Modified: Fri, 13 Jun 2025 21:48:20 GMT  
		Size: 9.0 KB (9013 bytes)  
		MIME: application/vnd.in-toto+json
