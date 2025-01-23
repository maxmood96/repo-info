## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:f7d26547b4f0d23b297c387252a8f22dab2b979148ac10365c2cb10009454a2c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:032273694aa2395cf04781a8a120fc421d131cbe9c9bbf1cc4bf2f25d6e7dd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.1 MB (142104564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead02c35bdcb8f655afb36690b265ba841abb012578413e11275d7da59848083`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
ARG package_version=1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:889191eec1e06c30b7664dfba1dba1d3f04b40b1cf6af4214dac90b998f32621`  
		Last Modified: Fri, 10 Jan 2025 02:01:02 GMT  
		Size: 53.2 MB (53150475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e3f6f3321126c30e5e5901f85529be69459ee79e3876fe4926cbf121ba800f7`  
		Last Modified: Sat, 11 Jan 2025 02:29:40 GMT  
		Size: 89.0 MB (88954089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8fb5d0c07980b72cbe1b03852cc4c41b02c9f55e01f3102bd5e2a26e38b6b59c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5189790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d4a92f314ca4ff8ee4db5791ba26dca5c3ac7c1c5f300a16cff06264b2dd538`

```dockerfile
```

-	Layers:
	-	`sha256:f2a7e2e2ea2656874c4d4212dd2b9ccc3f471d127ba930fdc2f76ff8171948c8`  
		Last Modified: Sat, 11 Jan 2025 02:29:38 GMT  
		Size: 5.2 MB (5181042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a319d7e6faec2e91898cea25675739d012378df7c9e3111c6584ff46992e6115`  
		Last Modified: Sat, 11 Jan 2025 02:29:37 GMT  
		Size: 8.7 KB (8748 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a6638140d02c5aff68764d59e873b9e149b595371f4c2bec02f4a19131dfcb13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.4 MB (140366533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a1d9410d35d0cb43f0c8c06f4b845df6534f5032eef9c7b618441538ffb2d72`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 09 Jan 2025 23:01:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 09 Jan 2025 23:01:37 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
ARG package_version=1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2dc99809e33185161e199db0b479b51cf3fb7470fd27c484aff50bdf9dcb5dab`  
		Last Modified: Fri, 10 Jan 2025 02:14:49 GMT  
		Size: 52.3 MB (52268196 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39979133675ea0f6dee32edeb2756fd2fa04f4d9715231652b3cd53c068f2dc`  
		Last Modified: Thu, 23 Jan 2025 18:51:35 GMT  
		Size: 88.1 MB (88098337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d7d7b413a220c2e02bae92e66b0ace5f62be8504b3480c0f5b62ff34f385b16c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5188655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76b1eb2042ac75c41b18c8106b0b46fe98c9d490a38340e14a067f6c90aa2682`

```dockerfile
```

-	Layers:
	-	`sha256:c6667d51f630fc9ca49b661ea996d1765a6a344a7db51e1c7f99df5ead5e129b`  
		Last Modified: Thu, 23 Jan 2025 18:51:32 GMT  
		Size: 5.2 MB (5179828 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25cb551dc0edefd18a057933d36f8039cd9bdaf6d1e410e7afd92c4d18f9ae54`  
		Last Modified: Thu, 23 Jan 2025 18:51:32 GMT  
		Size: 8.8 KB (8827 bytes)  
		MIME: application/vnd.in-toto+json
