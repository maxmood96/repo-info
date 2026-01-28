## `amazoncorretto:25-headless`

```console
$ docker pull amazoncorretto@sha256:b45d02343215b8456b0fbb3b4cc9de2d6f91e3f32fb60c7283a2a6fcc8e10dbe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7e2a007d664ed766dc5391de180c342564067a5a6ca550342f03a2c6a01dea39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.6 MB (157636395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:504333016ec243df8b3f384acbb7dbe50473b02dbeb9e4e340a730fdd8c9819c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:25:39 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:25:39 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:13:30 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:13:30 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:13:30 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:13:30 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:13:30 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:0fa079dacd9b36639e4d877eebffdb93a115a824e0b36ffbbb73537098b617c1`  
		Last Modified: Fri, 23 Jan 2026 23:23:19 GMT  
		Size: 54.0 MB (54023836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b2bd6c1e7031267a957c8412f391dbe7fcdbeb20c6f5b172e6a576f7ed848c9`  
		Last Modified: Tue, 27 Jan 2026 22:13:49 GMT  
		Size: 103.6 MB (103612559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:517271ddba934f0dc154c4fc3fdf65971cb31016d1abe5d7405220b3cb4a402d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5203822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52f8f95ae5f4d39b46f99f21e66afc997988f9e9b0162467e64a10459e764649`

```dockerfile
```

-	Layers:
	-	`sha256:4da60537361b255ea05514bbcb42d452ba332e6d643bbbeab3fc2226fd53d155`  
		Last Modified: Tue, 27 Jan 2026 22:13:46 GMT  
		Size: 5.2 MB (5194791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9cddc012f14250b1410e8bf8a1f04541f27df120a8a77bf2b05d3f3f5b76fd3`  
		Last Modified: Tue, 27 Jan 2026 22:13:46 GMT  
		Size: 9.0 KB (9031 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2e93b9bb07294e2656fe970587c09886d48aa3bdbad7ecbdaadad3e19b842d4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.5 MB (155452095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f98c456f3f8e34aa32f4a1c0bfb8fe9f09c22fbd70ed145718a41e685d3567`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 27 Jan 2026 21:24:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 27 Jan 2026 21:24:49 GMT
CMD ["/bin/bash"]
# Tue, 27 Jan 2026 22:12:54 GMT
ARG version=25.0.2.10-1
# Tue, 27 Jan 2026 22:12:54 GMT
ARG package_version=1
# Tue, 27 Jan 2026 22:12:54 GMT
# ARGS: version=25.0.2.10-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 27 Jan 2026 22:12:54 GMT
ENV LANG=C.UTF-8
# Tue, 27 Jan 2026 22:12:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:8f668074ce050169a9e353cb57e3886a670245836ecd3ffdaa8212e787a2ce69`  
		Last Modified: Sat, 24 Jan 2026 03:08:20 GMT  
		Size: 52.9 MB (52916638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17648fc590fe7c6d8d49ce63c1943888095135260642a9dfc6ab45a34f9d662f`  
		Last Modified: Tue, 27 Jan 2026 22:13:14 GMT  
		Size: 102.5 MB (102535457 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8baa5e097a12811e567936da0f3c0b56b88a5fcb0f7a6352409b83c4f4f8040a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5202725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d0828dfb9bf47e2baaf88ef26f2340aab95276b0bf93ef9ffb0884a6c8ae6d`

```dockerfile
```

-	Layers:
	-	`sha256:18974294bb4cab4f0cca31ddde7247d2ae8031e44316acc9c45a8c1110b4ff77`  
		Last Modified: Tue, 27 Jan 2026 22:13:12 GMT  
		Size: 5.2 MB (5193602 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:673441407d34da5afb565a0bc1acdaaf24d1562536b2ed5ee0e15eca5d3b872d`  
		Last Modified: Tue, 27 Jan 2026 22:13:11 GMT  
		Size: 9.1 KB (9123 bytes)  
		MIME: application/vnd.in-toto+json
