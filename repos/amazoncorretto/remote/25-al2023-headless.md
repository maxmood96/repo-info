## `amazoncorretto:25-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:ad2bcbd3a5c160aec879d2594dcdcd7b6ec99bc9340685e2d4abacdaf7e78fa2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ce2aed7fad891abc98e4c20d403d18367181ce93e21b3a9013676099f4951482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157622058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06287726bd6723989248c40413ffec71e650c53362ad56948baf1bab351ccc86`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:21 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:21 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:44 GMT
ARG version=25.0.1.8-1
# Fri, 31 Oct 2025 00:12:44 GMT
ARG package_version=1
# Fri, 31 Oct 2025 00:12:44 GMT
# ARGS: version=25.0.1.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 31 Oct 2025 00:12:44 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a6a2e926a3aceb887d70ba0a0cdc9e08ee8d333d6e1e2b76095173110288b60c`  
		Last Modified: Wed, 29 Oct 2025 22:37:42 GMT  
		Size: 54.0 MB (54001235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c72b93a14791c7a9beedec34cc9a57f19405495b431070d2ef8df9614332cda5`  
		Last Modified: Fri, 31 Oct 2025 00:13:24 GMT  
		Size: 103.6 MB (103620823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:58986ed63324972e68bd9b171e4559dc43bc2bde482259cbdbc6375d30267e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c833d01d70b56caf1460963d1e5528ece53276b3927f680114f1ffacb155dda1`

```dockerfile
```

-	Layers:
	-	`sha256:e0d1ff3ada7f20fb5faf5da8f2000517c2827c272b3ed44774ea25fa13b1df2b`  
		Last Modified: Fri, 31 Oct 2025 03:51:03 GMT  
		Size: 5.2 MB (5194783 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:84590b3bca1c059c78f9ac55013cd7e420f1e5c4e13e048227e03c82843bfdeb`  
		Last Modified: Fri, 31 Oct 2025 03:51:04 GMT  
		Size: 9.0 KB (9030 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:36e4f73567c0fdaf1b8a526d0e693c3dfccbde66522bebc72b1733360e6a97b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155465247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e09361006dba871291d9049ce5e3168e62c992a4236da579584757272d61c30`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:20 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:20 GMT
CMD ["/bin/bash"]
# Tue, 04 Nov 2025 23:16:41 GMT
ARG version=25.0.1.9-1
# Tue, 04 Nov 2025 23:16:41 GMT
ARG package_version=1
# Tue, 04 Nov 2025 23:16:41 GMT
# ARGS: version=25.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 04 Nov 2025 23:16:41 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:3cd303646110cfb66198d1d9eb777ff9d70a8bc53a53ab3c3446f6b686aa245c`  
		Last Modified: Wed, 29 Oct 2025 23:35:10 GMT  
		Size: 52.9 MB (52901851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857a3b55c1d229c3959d4b5d44284c68244ce4a01a2c79250512bf9797496cdc`  
		Last Modified: Tue, 04 Nov 2025 23:17:19 GMT  
		Size: 102.6 MB (102563396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:51d881cfadb42198928518a9ac0a5af0c5c306dfb354d562a0243284f503e918
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69687a4d4bf78a85fdbf054d8b3c2b57c9cfdbe9387b131269b23ba18f3f6132`

```dockerfile
```

-	Layers:
	-	`sha256:79dba41269b5df7d2b3253073eb39e5969d7cea605ea953743708ebdc1deb18f`  
		Last Modified: Wed, 05 Nov 2025 01:49:47 GMT  
		Size: 5.2 MB (5193594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f04686f739c926a1783f706001167b6f8b82e1aa2128d574b00a2ee08fea718d`  
		Last Modified: Wed, 05 Nov 2025 01:49:48 GMT  
		Size: 9.1 KB (9122 bytes)  
		MIME: application/vnd.in-toto+json
