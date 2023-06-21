## `amazoncorretto:11-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:f08270a29c5cae0a22a2030fe4c8a751e21d426c37ca170cb795ca49a17f66b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:622ed48f17fd161c7b7f1a65586fef39708f8ab5435386e193dcae374b25c897
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.8 MB (128800463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d30ba23ee78ffec054a4ecb05307ffd3c2dc08eb65f42f414c041751417aff97`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:19:53 GMT
COPY dir:63b753315cbc8a46d071e63503518488c1171a5492a355d5915f823055385aa8 in / 
# Tue, 20 Jun 2023 22:19:53 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 22:54:31 GMT
ARG version=11.0.19.7-1
# Tue, 20 Jun 2023 22:55:26 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Tue, 20 Jun 2023 22:55:27 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 22:55:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:a802d1401e244b250dd1bf27864d0c9b6b46b98aa0b6061bce13e9dc82bc082e`  
		Last Modified: Tue, 13 Jun 2023 21:23:05 GMT  
		Size: 52.3 MB (52256179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:254e9723de16ad3267e28e8c1bc1142a7a8a613e91cb8679ec54ef561dcc65fe`  
		Last Modified: Tue, 20 Jun 2023 23:01:24 GMT  
		Size: 76.5 MB (76544284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5bee7e6a0fc0014d3b8dd8c4c4eefb5ab828fd7a39eb4ff822ddb7b5c84f6108
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **127.0 MB (127019676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:878ac4718448d3cd8d7a66300434004ba83a1fa10587f3319fbab97c57a2f8c3`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 20 Jun 2023 22:39:47 GMT
COPY dir:4c02dd87f965b9a0652991e3f4ecda20fc951006541ed9dd1a7ea47d86a8e856 in / 
# Tue, 20 Jun 2023 22:39:47 GMT
CMD ["/bin/bash"]
# Tue, 20 Jun 2023 23:23:46 GMT
ARG version=11.0.19.7-1
# Tue, 20 Jun 2023 23:24:37 GMT
# ARGS: version=11.0.19.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Tue, 20 Jun 2023 23:24:38 GMT
ENV LANG=C.UTF-8
# Tue, 20 Jun 2023 23:24:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:0dfb0edac9a78a1d87befb4107fecf3f30b0eb9715fcf5417a32ce37b134d95b`  
		Last Modified: Wed, 14 Jun 2023 03:06:34 GMT  
		Size: 51.3 MB (51304677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fde2380703e693c3dbed0532c4d29fe825d9f51ee3fd73f0ba8fee4dec02fda`  
		Last Modified: Tue, 20 Jun 2023 23:29:39 GMT  
		Size: 75.7 MB (75714999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
