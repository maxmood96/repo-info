## `amazoncorretto:21-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:dfdd57d11dd9fd4fc0df89f21d693a971e1d4bde40ef3b5633a068036a7a7bf1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cdff315482c77d2d1427c811f1e4fe04f4d7d19ff492a41cb3b7b7a51c295b99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.5 MB (144543006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6cabf6ab023736024463a8ecf6f8b93cb0abcbbcceebe3b3662e5b6869a5e80`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:26:29 GMT
ARG version=21.0.10.7-1
# Wed, 15 Apr 2026 21:26:29 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:26:29 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:26:29 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:26:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21edaa9e22c9bfe64c5aa79068e8e4ed7bea41ff8cf141f4286e7277c3a8be75`  
		Last Modified: Wed, 15 Apr 2026 21:26:46 GMT  
		Size: 90.0 MB (89971752 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc01a75c8601134b3b57321ad2b636eb8d6a0ef6536cc651e5cf7a975a57ece0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5225443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad61479344c4cf256dce7c99d5f9c92a535b6b2cb218768670232507c60e5b26`

```dockerfile
```

-	Layers:
	-	`sha256:d8c32c2e401f3112f19850022a505f5540efc130bbc0bbd6c12a954618142e86`  
		Last Modified: Wed, 15 Apr 2026 21:26:44 GMT  
		Size: 5.2 MB (5216395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c6c9e93f0c86c1d36990457bb17ebc20d43c1921c9f06c31ea2bbd745ae9cf4a`  
		Last Modified: Wed, 15 Apr 2026 21:26:43 GMT  
		Size: 9.0 KB (9048 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9eb8605d3b39947f34a32955961bcd06de19d8df45d73d472c4fe6f25f64f20e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142555860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be15d12669ce6ead111e83030d259b43ffbe407dfca8a89f0ec948cffebeff68`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:39:40 GMT
ARG version=21.0.10.7-1
# Wed, 15 Apr 2026 21:39:40 GMT
ARG package_version=1
# Wed, 15 Apr 2026 21:39:40 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-21-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:39:40 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:39:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:015ab1ce9e8479d680972bcbfb365fdada5cd638322b99699dc80c9facddcc1f`  
		Last Modified: Wed, 15 Apr 2026 21:39:59 GMT  
		Size: 89.1 MB (89113121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:82a4ed7c3508580e3d028260204eeef9f332691b6d0d93f179f8a48ca98cb42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5224315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6690a6d4ba7d4509b9ca7ec07689e9d74feed45fb72fd87456699c5395d64759`

```dockerfile
```

-	Layers:
	-	`sha256:9a4e69c1be6d9811766d8c39999dc290771c848ddbd7b80727cc8724cbf294d0`  
		Last Modified: Wed, 15 Apr 2026 21:39:57 GMT  
		Size: 5.2 MB (5215188 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3d2982dcea964312d50f240c4a9a397d3dd4b2b41b014d99ce27b5bc7b74c1`  
		Last Modified: Wed, 15 Apr 2026 21:39:57 GMT  
		Size: 9.1 KB (9127 bytes)  
		MIME: application/vnd.in-toto+json
