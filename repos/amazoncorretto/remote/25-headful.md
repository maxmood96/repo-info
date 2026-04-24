## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:86f32f5feae4759c18729812fb9ca71a18637db1f988c668fd5cd8d00c98e90d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b87e1e01b4df214a3d0616fbfc3f2cb54247c7706ed931e9562c9f4edfff95eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159009092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667e2a6e202f123b92d4882b5c9583d217be0640beb940aaee7f1edf1755ee8a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:40 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:40 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:57 GMT
ARG version=25.0.3.9-1
# Fri, 24 Apr 2026 00:13:57 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:57 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:57 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:60406c832328f9a4f3aa21eb9cb5b2182d79ad008cd21f0bbac4517c1836be2e`  
		Last Modified: Tue, 14 Apr 2026 01:03:42 GMT  
		Size: 54.6 MB (54569705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ea91f6d1b50ee791cc0e8775d1b154e7acf159696a96b8f3fcd6f0656d46c3`  
		Last Modified: Fri, 24 Apr 2026 00:14:18 GMT  
		Size: 104.4 MB (104439387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:948726891e6efb9a5f7b98eef95ecb7fc802fa26611488ba5c89a9166b7c845f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e65de9a96d208ef09820ebb016e5243c6c7527423e631b1fd5ded5c226a74b16`

```dockerfile
```

-	Layers:
	-	`sha256:865d374b1e673cdd476d59585e45ae81098fc69a8706432dbf3acfa96153de33`  
		Last Modified: Fri, 24 Apr 2026 00:14:15 GMT  
		Size: 5.2 MB (5227475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:394fcfb49875decaf95af581ccdf69f044f02ee52e321cb222add4d1a6cb354a`  
		Last Modified: Fri, 24 Apr 2026 00:14:14 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0def29447f208c9f185705af129e8f3f901d5dde97cb54e75dcfdb9d4dbae624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156843230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:065e79921063b43ae59f1ed781115aeb6478aa8d2615f6f48d1bd6b3b364d9ac`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Apr 2026 00:02:02 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Apr 2026 00:02:02 GMT
CMD ["/bin/bash"]
# Fri, 24 Apr 2026 00:13:12 GMT
ARG version=25.0.3.9-1
# Fri, 24 Apr 2026 00:13:12 GMT
ARG package_version=1
# Fri, 24 Apr 2026 00:13:12 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 24 Apr 2026 00:13:12 GMT
ENV LANG=C.UTF-8
# Fri, 24 Apr 2026 00:13:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a89c935522476873ac76a02a8b4103cba17c6900bdcb1d98998ed64657edf59f`  
		Last Modified: Tue, 14 Apr 2026 02:24:36 GMT  
		Size: 53.5 MB (53452253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad84e8befa4e3899a1860d7a0bf4c4dbb512de78fe48cf55c4bed1a806b1a867`  
		Last Modified: Fri, 24 Apr 2026 00:13:33 GMT  
		Size: 103.4 MB (103390977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:110eacf9ddda17df608a587406b29d205ea7615cfb289eeb24a6481ba22a74dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b501c163e0afedea0c70b4f0a2dcd7b7d1ccc211309cf66bf8e0ca33549915c`

```dockerfile
```

-	Layers:
	-	`sha256:11147bb7cce1672f54132f93d04f9c289eb51b68b0fe17e62ef680969d3fda28`  
		Last Modified: Fri, 24 Apr 2026 00:13:30 GMT  
		Size: 5.2 MB (5226290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4b4adf655955e65a216641c7cdb8c5e263d52bf953271a48922a4970a7a5afd8`  
		Last Modified: Fri, 24 Apr 2026 00:13:30 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
