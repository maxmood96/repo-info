## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:c8f5ac7e6a1c7e59d9d568104ab31de583b9ea390867bd8a6e3f2ccdbea287c9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

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

### `amazoncorretto:25-al2023-headful` - unknown; unknown

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

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7e44a15f439361926c1caeb89c6caa09ddae7269bcba00cf7eed81ecb04a420e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.2 MB (156179277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5149108126eec88f96866122d46c3f793287c4bb842dd2d28f8b80e7ed659055`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:13:15 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:13:15 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:13:15 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:13:15 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:13:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f03ae37e79cc5e91f16ddddefee021a1a03f4fef52c47b20b896ac986ce2672`  
		Last Modified: Fri, 31 Oct 2025 00:13:51 GMT  
		Size: 103.3 MB (103277426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6bf9a93e78c81ce3f91c2af955f89c75ac52b5bfb80c2f9d4af4e7990480a5a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5228320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ef3161466943d385d18d58c1fec8dc4428465d7e1f9104e39a66b1a9d10db28`

```dockerfile
```

-	Layers:
	-	`sha256:825f268abdfa5593dfdd2c28e41418b4a2424cc4a9fc307c77656659ef3c31c4`  
		Last Modified: Fri, 31 Oct 2025 03:51:02 GMT  
		Size: 5.2 MB (5219022 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f962293b62a8e660a914170274ea0802a87d10fd40f180fec1469e148a7a4bb7`  
		Last Modified: Fri, 31 Oct 2025 03:51:03 GMT  
		Size: 9.3 KB (9298 bytes)  
		MIME: application/vnd.in-toto+json
