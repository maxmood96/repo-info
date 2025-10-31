## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:e6ed42c02a357cfb452134eb72df6d0112ef395ef9f62e334cb1460c848b4e7f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:abec70ce90e33ab53648997d26c6bbe6863a30f0354dba4cddc46f3ba5f3b3c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.4 MB (136386406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ff4841a7799e5d17fa9df518c20f4d0c6d1d6fcc0366fd97497c986842ab77b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:03 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:03 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:03 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:03 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28034115598860a6c4c9b8450882ed814b7f2409409437f1badab65b556386cc`  
		Last Modified: Fri, 31 Oct 2025 00:12:39 GMT  
		Size: 82.4 MB (82385171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7fa29002496621eb2d038700471b28fb1e907e6734bf3c0eaefb32b37d328864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2dc3bb575d4214da15ed0aa7770c044ed18cf7bb19066320700a00010e9acc`

```dockerfile
```

-	Layers:
	-	`sha256:09370190d5548cfc7ed7df611ecb78d2b3771171057d24eb33a0cb7dfd83bb7f`  
		Last Modified: Fri, 31 Oct 2025 02:45:05 GMT  
		Size: 5.2 MB (5182896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5c4d6761de22155b26ebbbebb3abc5b71ec0aa66cfd47c5bfa181fcf8dac76e`  
		Last Modified: Fri, 31 Oct 2025 02:45:04 GMT  
		Size: 8.7 KB (8713 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f7ac8d2ff14a80b0e77458ceb53a7f2a9c8bca25206e3dd119d057d13c4ddbbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.7 MB (134703349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9aa04abf419af14ad1c3f81175ae8b9b0e5ce9f67d835f905f593cd1b7898269`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:28 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:28 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:28 GMT
# ARGS: version=17.0.17.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:28 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48b29b2ed0f2c4add970e7ba392903391f13ffcb06b0ad8f121b7085555ddb55`  
		Last Modified: Fri, 31 Oct 2025 00:13:00 GMT  
		Size: 81.8 MB (81801498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c51167ea9b826d4c4324869a88eb1ec0b2417d4f7073147d830325880398c3fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4600a291e06e0ec4bfab1afdb69a30e6e2c45c4ab0254d9328c2ae4039e3b0c`

```dockerfile
```

-	Layers:
	-	`sha256:24ca6d98af32745a100a2d32e1041706329c1fb9c7c48b53f44ccafe3d6ae9ac`  
		Last Modified: Fri, 31 Oct 2025 03:49:24 GMT  
		Size: 5.2 MB (5181684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:901382b9d9427707113ccf31baf2387e1c6835ee66ecfa1e9a79a8d1d84cc874`  
		Last Modified: Fri, 31 Oct 2025 03:49:25 GMT  
		Size: 8.8 KB (8793 bytes)  
		MIME: application/vnd.in-toto+json
