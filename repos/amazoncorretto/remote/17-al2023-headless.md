## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:5eb11aba9ee23e685041918a64e9880c9cd8494b1cd8b6ecc33c7bad9a8b86e5
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:555088f7e07cbc2199348a8052d6c7e5ce348d1749c106d1d5573c64786f09fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.1 MB (136053120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4764fac7392051efe08018cf6586b492025943277211662e0cc6e22149ffe07`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1c3112c87ab2d6209030c22629180b5d1958fca3765b3cbcfbc9bcfa1ee6e425`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 53.9 MB (53880920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4415142c46099c57ee5f0e1bc4f429dceffa2d994a3f75c78bae1245ae579206`  
		Last Modified: Thu, 01 May 2025 21:08:17 GMT  
		Size: 82.2 MB (82172200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3d86803893fb414a838524d33c8cf74262d5cb1c15f96eeb8e10c250524c2af6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5177016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f67956eeabdad875ede056be5ae28df0554b9647892aa2eaf3b1dc740f14df4f`

```dockerfile
```

-	Layers:
	-	`sha256:eea9a9206462831c0deb3666fbb9f84bca73254971ee0351d3f149075b47a63d`  
		Last Modified: Thu, 01 May 2025 21:08:15 GMT  
		Size: 5.2 MB (5168265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de0d5ed9a5ce02b7c8ecd10301e3b5e8f0d07bf26848f85aef5679419bd1b863`  
		Last Modified: Thu, 01 May 2025 21:08:15 GMT  
		Size: 8.8 KB (8751 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:044a15f1830615e3ee1db47383d4fc5e75cccfdaec6a9bb86228bd74b4f81031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.4 MB (134420066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:627d7d7f37b477fea110420080e16e2f93704205030f00d4f1af50228e873ce1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5804bd91a568b15c202af6e01f57d869865af0d532f8773d8faefb503ef0bbfe`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 52.8 MB (52811047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c691e39f80d2d604d0a3f8c7b32c0ec31c5945f95690c3ae912b53f1d757f93`  
		Last Modified: Thu, 01 May 2025 21:17:45 GMT  
		Size: 81.6 MB (81609019 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eda8a25f2c65728710c1d0cb70320cba08c29a4f315da634ef4aacee6529565f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5175884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0815ebf7e019ebc65869615c2fac1174baa1725fae1224e1095019ef2b5378c`

```dockerfile
```

-	Layers:
	-	`sha256:f88f9f533ba0e1b613bb1a5a8defd4bd21e02578d1b5e7512edbcddedfaa2946`  
		Last Modified: Thu, 01 May 2025 21:17:43 GMT  
		Size: 5.2 MB (5167053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec21958c77a3963e0f47fc9ce38eeb47fef03bd6b4973870672d9c92879344a1`  
		Last Modified: Thu, 01 May 2025 21:17:42 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
