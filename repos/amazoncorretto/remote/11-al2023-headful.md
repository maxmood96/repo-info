## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:706b362fedb1133acdbaa29ded711be9d5a90d66e6bef62e498648e8fcfd5eb1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e113a02331110f75da397d5e29949e09c04412b4cbdf410c4f5b04ec53195b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131278691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6eadd15fced4e3bfd9d0ff31f39eba739289836a39079d5416fa5729156f086e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:10:58 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:10:58 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:25:08 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:25:08 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:25:08 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:25:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:f24558f24158eae4a7e3aceff47ef1d2c507935ec782c707d42d4166d9c76fca`  
		Last Modified: Wed, 08 Apr 2026 02:13:20 GMT  
		Size: 54.6 MB (54571254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58736277e7e2204ec2b04c2a23fdf7b9876d7f3a26c40eb2a3abc2a80e924fa2`  
		Last Modified: Wed, 15 Apr 2026 21:25:25 GMT  
		Size: 76.7 MB (76707437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c6d230821cc45da19554cb219d370c52cf58930fc5bceb3b0042f90a1f7f71c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2aa5b67309bf9152d5feb69eb61407057aa75582b3e615ebd58f3606186290e`

```dockerfile
```

-	Layers:
	-	`sha256:571a63c938bab6cae0bb7cdb6dc00ec7487b4f55d719e74105eee78226102561`  
		Last Modified: Wed, 15 Apr 2026 21:25:23 GMT  
		Size: 5.2 MB (5228692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0fe126a34ff96ccb3ad13345beba2a8d96a10b12081dd1ef13658d521e457ba`  
		Last Modified: Wed, 15 Apr 2026 21:25:23 GMT  
		Size: 8.9 KB (8906 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:3ae36e830bac2b3de4584a5c134b7dd064aaa8246632293e24c0c114753f0670
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **129.4 MB (129398835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941d93fc707336c4056b0dbcd21433699d317f1016c1a609d72e1bcc24912e40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 15 Apr 2026 20:11:08 GMT
COPY /rootfs/ / # buildkit
# Wed, 15 Apr 2026 20:11:08 GMT
CMD ["/bin/bash"]
# Wed, 15 Apr 2026 21:38:37 GMT
ARG version=11.0.30.7-1
# Wed, 15 Apr 2026 21:38:37 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.${ARCH}.rpm" "java-11-amazon-corretto-$version.amzn2023.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 15 Apr 2026 21:38:37 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 21:38:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0f6f50638ec30a0ad5245c92db189371df09b6d7d9b5519369c28833dbca2ef8`  
		Last Modified: Wed, 08 Apr 2026 02:13:16 GMT  
		Size: 53.4 MB (53442739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f650844ee60e15ea2132c23112e01e01ec8ed43772e2921672070d6ee37d9c`  
		Last Modified: Wed, 15 Apr 2026 21:38:55 GMT  
		Size: 76.0 MB (75956096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f81d4a7fbe28f7c9624bfbeaca1286b24d270a28df3cbddd059344d6bbbd22c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5237299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:941d7bfc38dd853afab4b83da6a6ff0ef7d0cde7d08016c7c282afc9f6ddc662`

```dockerfile
```

-	Layers:
	-	`sha256:6318cd86d391020339710ab9ef70c1020356832e87ee8a88c5813d173270e780`  
		Last Modified: Wed, 15 Apr 2026 21:38:53 GMT  
		Size: 5.2 MB (5228313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5c6913cff334a80c9fcbf6fc0d1d8756d5a5bacd4f3a417af7506f7f8826c7c`  
		Last Modified: Wed, 15 Apr 2026 21:38:53 GMT  
		Size: 9.0 KB (8986 bytes)  
		MIME: application/vnd.in-toto+json
