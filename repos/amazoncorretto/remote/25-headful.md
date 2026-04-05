## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:9c56d0868861bd44884e199a45a50f042106affae4e76fa5e14c592c45e554db
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:464026d998deaed9cede7d8f4aac5c58f4909cba79b0a3f44d835b5a44702fbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.9 MB (158903514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550d80dfba6762d858dbd4b150c7c53da340d3f1cbcc8839763b9b64951c4783`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:16 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:16 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:15:19 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 22:15:19 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:15:19 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:15:19 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:15:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a2488c40110fb2b90385f44d9af6173894e14350935e38653aee164551cb70d6`  
		Last Modified: Thu, 02 Apr 2026 00:19:16 GMT  
		Size: 54.6 MB (54571303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f43964d9e337b6375d7bfb6120ecc9b2d8816ed53fb5d12616a990bf8e1f009`  
		Last Modified: Fri, 03 Apr 2026 22:15:38 GMT  
		Size: 104.3 MB (104332211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:257b733e17e5e9fbfe08f600847e00d34e98a6b99e63f0e70b9e07557f22ca76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcfaad67e8d0fceae51089c7cbd89d9a2e60460c1c9ba5f9c50591012bccf4e`

```dockerfile
```

-	Layers:
	-	`sha256:b43679cfebc70cbf9b271a0f7aa237f0059c7cca44bd65b109a987addbde065f`  
		Last Modified: Fri, 03 Apr 2026 22:15:35 GMT  
		Size: 5.2 MB (5226662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:388af5c78bf820dc942a6f72252db1f48cd6367c50588bf1ba14e789a36f16a4`  
		Last Modified: Fri, 03 Apr 2026 22:15:35 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1dd2a438bbba7ed2e252c5e0a1567169c022c666c4c6d69de07f9af55517fd59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.7 MB (156704684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8491029f92db7b03361302e80c3c3facb77260bd46dca54fdedc7d1bbd8368cb`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 03 Apr 2026 22:01:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 03 Apr 2026 22:01:04 GMT
CMD ["/bin/bash"]
# Fri, 03 Apr 2026 22:14:38 GMT
ARG version=25.0.2.10-1
# Fri, 03 Apr 2026 22:14:38 GMT
ARG package_version=1
# Fri, 03 Apr 2026 22:14:38 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 03 Apr 2026 22:14:38 GMT
ENV LANG=C.UTF-8
# Fri, 03 Apr 2026 22:14:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:cf8ff26f8ca2e7db6c1eb2c69aec532f89cf3016cc84f77de00b260ba62b2ffc`  
		Last Modified: Thu, 02 Apr 2026 00:19:15 GMT  
		Size: 53.4 MB (53442825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9132c3f0fe8680f2ca74763ec0a7f78c885500fb0c39a78bd9c6bc199475eea6`  
		Last Modified: Fri, 03 Apr 2026 22:14:59 GMT  
		Size: 103.3 MB (103261859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d3499eb94d29ca5a2b982f9d927b038087ea05d2d461e0623cfff9f2f0541d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5234936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eca9e0f128bceb35b7f1435c8d8e77a91297cceb3b4771020bcfb9443a86856`

```dockerfile
```

-	Layers:
	-	`sha256:4c59c9147dcc7abedebec48fd6903f211824e9f1b5f63372efbb67d31c7a9e4f`  
		Last Modified: Fri, 03 Apr 2026 22:14:56 GMT  
		Size: 5.2 MB (5225476 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11283017ef1884f7664207287eec7b9657acccc1aabb8323728ebe4906f9cbf`  
		Last Modified: Fri, 03 Apr 2026 22:14:56 GMT  
		Size: 9.5 KB (9460 bytes)  
		MIME: application/vnd.in-toto+json
