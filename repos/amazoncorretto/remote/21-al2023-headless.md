## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:95570d2b5359bace005b429a22b7bc080e8804ea911dffd519a2f67040487094
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:679606ca6308925930e6807e68d3b3dff210a33bf088032bc41fefbcb88a7dcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142094041 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e06b1c4dfa55528971a3e2d5c5f25180a8e50e43627abf1eae75376c5f2144d4`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09b36aa967eec5affa2fc488aefbe484978558f601663fdb7197a8afc992cf06`  
		Last Modified: Thu, 27 Mar 2025 23:58:44 GMT  
		Size: 89.0 MB (88970752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1687dc554969f60405de5eb65fc8b8b453eebfc3fb9b1c97ac91dca0d0cda14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5170078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64496522b5a27d086a9fb32eea1da3db2d589edb262354245384f97dc16d4684`

```dockerfile
```

-	Layers:
	-	`sha256:a719366dc8dc20b39f10ea1d760b558c679f012a09543c71f08ebee3630c6284`  
		Last Modified: Thu, 27 Mar 2025 23:58:43 GMT  
		Size: 5.2 MB (5161330 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d303239e65f723614a6c4b417aea8c8bacbe39ec08c21e948134e92aa2a35e76`  
		Last Modified: Thu, 27 Mar 2025 23:58:43 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:67d9633abcf6b802cdf5f7383c1b256d67c10f024f8d019af66d7d114966a1e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140354023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec77326ed892124f194c2740c290f5a955ab67b85e2c9b303cbf69b9b45b803`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=21.0.6.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78541e6db98594811543fa73b3e4b93928418742dd80cba3127f8a56b8da9b63`  
		Last Modified: Fri, 28 Mar 2025 00:21:17 GMT  
		Size: 88.1 MB (88106033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cbb2ddd5413a94b84dfddfd63da5862622959c00a3a43f4307a9b5c419728088
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5168948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf7a1a890c9f56d92994b2d41d806f2a1af8120e943a430bd3346bc4c2ece702`

```dockerfile
```

-	Layers:
	-	`sha256:fd13de99d9cd981e3c05ecee7df650804263e640639803253e8f828756458c2b`  
		Last Modified: Fri, 28 Mar 2025 00:21:14 GMT  
		Size: 5.2 MB (5160120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6843a405c369fb69f83f6b8017f5453e7f6cf9d439f46e84b30f6065006f22`  
		Last Modified: Fri, 28 Mar 2025 00:21:14 GMT  
		Size: 8.8 KB (8828 bytes)  
		MIME: application/vnd.in-toto+json
