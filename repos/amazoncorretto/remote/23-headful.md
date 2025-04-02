## `amazoncorretto:23-headful`

```console
$ docker pull amazoncorretto@sha256:01520155b09b540c489ad0038b49cd1d8e9d0faaf685b083aa0aa6cce70ff54a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0e597090a19cf35a891da006bfc0f7d3bf802fdb15eb2e6a9fa82ee0a4fcef56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.9 MB (149866613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f1a426c253addc94a0e412d9ab273b580ec62b48c576975abc6ca4c666d1aae`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff496c344df085754666a6a320560349df1cd4bde56baeac577a251c51d6ed59`  
		Last Modified: Wed, 02 Apr 2025 00:02:04 GMT  
		Size: 94.0 MB (93959560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1cde0d14809ec508f5c0eb0857e449d6051293220abe5831037d5c8135bc69fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5464715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5578357fbe15c4f48ca908f2eb8abe6eaf731c094e4aa40af6f35f5c3af55bb6`

```dockerfile
```

-	Layers:
	-	`sha256:472e633e6c2fdab9dd242ea6a9a8ec73297df170b149aab1d8c8633fb99bd194`  
		Last Modified: Wed, 02 Apr 2025 00:02:03 GMT  
		Size: 5.5 MB (5455466 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f828d805107bc9ce56a993a54a46f1b74883b7405e79bc7610972960f03ee9fa`  
		Last Modified: Wed, 02 Apr 2025 00:02:02 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6017bc1acee9bfbd744746a3f706ce21c85a89e17ac59ac4733f948052ae5ef5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.1 MB (145119546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80163a531af72601c5df3f76d605390c2f830a03027784872361c3e949924872`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=23.0.2.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=23.0.2.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-23-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-23-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-23-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-23-amazon-corretto
```

-	Layers:
	-	`sha256:92a376874570d50aaa72a4435a5b15fdfcdc3099600b45751b2c0705bd2c65f2`  
		Last Modified: Thu, 27 Mar 2025 02:43:04 GMT  
		Size: 52.2 MB (52247990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5195ab738439569e94f052c447d6206746601a4a21a426fdd8ba032ceacda13a`  
		Last Modified: Fri, 28 Mar 2025 00:24:50 GMT  
		Size: 92.9 MB (92871556 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0556528910f1f4dbaeb6457a881e157386eb747359c66f28e3ea73f4f96eb18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5196733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0916cd200b5fcef067d6dd7093fe258cbe7622f2ba5bbd3214a24bfe88018c`

```dockerfile
```

-	Layers:
	-	`sha256:7a5820853da8c87cebe0b060bec2ec0b99f51f9164ca91571f4a7a854ac15fb9`  
		Last Modified: Fri, 28 Mar 2025 00:24:48 GMT  
		Size: 5.2 MB (5187392 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b86614921f8a9dadfdc186616835c1a6339b2e8b8fad63d2481b34ab091c5fdb`  
		Last Modified: Fri, 28 Mar 2025 00:24:48 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
