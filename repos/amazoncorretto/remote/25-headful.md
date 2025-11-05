## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:c4af4b83293bb6f338fd9b09acf9ccb1f77a7f90fdedac5bb7f71c34876b7de0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e67fe82821be4c3292a1ddcd1521b2f99cadb5716e2dc7325c84a388bba1f615
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.3 MB (158333300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1b47ced037b00a4bdd91f8fb6290f7c0fbec1ab5dba42aebbc3d48e197e4253`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:50 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:12:50 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:50 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:50 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:50 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55b2c38ae8cf5b3caa78508f2c504e33daa80dd9962c320d1107b354d7e565de`  
		Last Modified: Fri, 31 Oct 2025 00:13:31 GMT  
		Size: 104.3 MB (104332065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d2427f1eb6478265cae879e1834fd8aaccc67323873636292cebf32d2f94b39a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5229415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65a418a1a1a9d88ee5f424d0fea7a41e4a65ed7267f1a0b7e1b7a730a454a06`

```dockerfile
```

-	Layers:
	-	`sha256:a9c5d94a75a3b0eb1d5a0a4c8748d9f9606c608cac913559232b26f8f1ba6d5a`  
		Last Modified: Fri, 31 Oct 2025 03:50:57 GMT  
		Size: 5.2 MB (5220208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f494b2292a29224879490f4c85a034fec1c1980b6ce59f735674ee35364c6dd`  
		Last Modified: Fri, 31 Oct 2025 03:50:58 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2ecff325efcb978c1b1dc949295d3247775da7ef9ac593b2a8542455449eafdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156178667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:780391fc586064c59301822e910ecfb059b5b5dac43a5970d718f0a67368a394`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:16:42 GMT
ARG version=25.0.1.9-1
# Tue, 04 Nov 2025 23:16:42 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:16:42 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:16:42 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b85afa25beac1d0bc306619ce763a649516bf26a0c575f81cef3ef50a9ee11b`  
		Last Modified: Tue, 04 Nov 2025 23:17:23 GMT  
		Size: 103.3 MB (103276816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d2831526209a9fd1fe35151dd704feda3f30145cbdf05112d108152b5e68b673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb2804f6a32d7b37dce5eae9bae25f14923cc568ce448463b8e9314da2110871`

```dockerfile
```

-	Layers:
	-	`sha256:1d6a7e26cff85b8540888c4aae20f5fcd54211ebce3e891c520bc2c66fb2da0b`  
		Last Modified: Wed, 05 Nov 2025 01:49:43 GMT  
		Size: 5.2 MB (5219022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:317426b955a95c5e2b7233313132c210620d1d140bbadc07ce8ebd61059180a5`  
		Last Modified: Wed, 05 Nov 2025 01:49:44 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json
