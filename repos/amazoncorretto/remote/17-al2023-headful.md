## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:2e96ba8002ea8e8dcc82a004168b79459592739b27b2e9171598c4b8fb1acff5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d434663d401aabaf3dbb76ddd9884db2629a7966391b7b194acb7cf42d6c18d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.7 MB (137652042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efc81684b04bfedbfb95b0454907fc56b0ae23f71660c41905dfb746acd19a04`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:34 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:14:34 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:34 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:34 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70f96d1ea0f25d1959b2f9cf55230e743a52bcaae611dd99495a399a4f9ad6f7`  
		Last Modified: Fri, 03 Apr 2026 22:14:52 GMT  
		Size: 83.1 MB (83080739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2622af4d57d305e2f0deec07e70fe0c66cc7b67d616c09e38df0302b9cca6b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5223817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b33dc5f1713ad793d7c9936702ec8499f29d331fa3bcbfa543919b73759c10c`

```dockerfile
```

-	Layers:
	-	`sha256:b1d13d1816be952e72034ca6114a8d9cb4f08eda07491a997f7c0ca1ad7c29ae`  
		Last Modified: Fri, 03 Apr 2026 22:14:50 GMT  
		Size: 5.2 MB (5214769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6cd3301a4b7b8ca75f6d5947a36917c560432f55a1069e160a5da07a3c61636`  
		Last Modified: Fri, 03 Apr 2026 22:14:49 GMT  
		Size: 9.0 KB (9048 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3e7835996483b39255d20cf890c411892b734d07581005ea7f1ce88afa134b5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **135.9 MB (135944733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb033846adc38bf09da546aa86d54a085615d429615d203807258c6152036690`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:13:51 GMT
ARG version=17.0.18.9-1
# Fri, 03 Apr 2026 22:13:51 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:13:51 GMT
# ARGS: version=17.0.18.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:13:51 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:13:51 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10e24e6be04a8c67f557e99db72e30c5a59b435a818b6dc66a2538643a907825`  
		Last Modified: Fri, 03 Apr 2026 22:14:10 GMT  
		Size: 82.5 MB (82501908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:171248d164e28d364932682b40f38ca8164553bda83cf4c26cac7a019416d55d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5222686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8978571ffc970ddda529534ac3bc67c9f4d30bb597f1b8ede79ea44fe16fe31f`

```dockerfile
```

-	Layers:
	-	`sha256:d81f4d571714b4781d977bac9fab930c0a64f168b8f4a169b1db2db6ae7b2668`  
		Last Modified: Fri, 03 Apr 2026 22:14:08 GMT  
		Size: 5.2 MB (5213560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88517492b6704fca89bc56571a1728fee8c8d4c140a04ae3723642c713c09a11`  
		Last Modified: Fri, 03 Apr 2026 22:14:07 GMT  
		Size: 9.1 KB (9126 bytes)  
		MIME: application/vnd.in-toto+json
