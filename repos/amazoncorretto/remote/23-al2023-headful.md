## `amazoncorretto:23-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:d71f7a4518303df66f35d2f7aa2497324636bb714f21be7bebd34245efdb7abe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e5659a43981228c56261774e85c9db049050ee79f8f9dbfacd13caee9bcc6fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.0 MB (146979793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a14e857a9495e9ebe9104ac947b054b7fc31e7f9bffe79f53d08dcc150957b20`
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
	-	`sha256:76cc64d6a248b04196e7ba8dc6c3e7ff1d81e82f9d332d320529c20ed03cc7f8`  
		Last Modified: Wed, 26 Mar 2025 23:27:10 GMT  
		Size: 53.1 MB (53123289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f9e5e7840179d1503fc02e709068963f430690d59da2f720d2319effa0ffcb8`  
		Last Modified: Thu, 27 Mar 2025 23:58:49 GMT  
		Size: 93.9 MB (93856504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de383246184d282e8e12903a269423f74907a6e73fa906a3c6efe4c9a4ce9014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5198649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ced0ceede1f1cebe3aa56775c3db765dfa2ad68bad06c4c4b2a81937c00d9bb`

```dockerfile
```

-	Layers:
	-	`sha256:9661afc6835ab543d97316878a0fb6ace996930d3309fce71c5bfbcf10d85bf7`  
		Last Modified: Thu, 27 Mar 2025 23:58:48 GMT  
		Size: 5.2 MB (5189400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74d1f02efbac7858f6b6055e7bb12c4c058816eb560f97959114245fb9882526`  
		Last Modified: Thu, 27 Mar 2025 23:58:48 GMT  
		Size: 9.2 KB (9249 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-al2023-headful` - linux; arm64 variant v8

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

### `amazoncorretto:23-al2023-headful` - unknown; unknown

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
