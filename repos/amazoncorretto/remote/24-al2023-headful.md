## `amazoncorretto:24-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:52920cdefb97f639fd260bba7444521f7ab2bca0a81dd9dea70e0683ff57a695
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b38b09c72815a14a3914a9bbb91aca3eab02bd18ea14dba89cdfa0f0eac00973
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (158975939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4cf0f542bd2915c77839d3bc1ff81fd6c61327d200422745a48c0044f47f1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 15 Apr 2025 21:50:45 GMT
COPY /rootfs/ / # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:1cf9fb914831ab202ad1756fe44227d7c88c49394a5cc9749ad863e76989673c`  
		Last Modified: Thu, 17 Apr 2025 22:49:09 GMT  
		Size: 55.9 MB (55906521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0891073e6cb5310f5a3dcfc310e901dc36c5a40077cd4871c2f0eb88dad044d`  
		Last Modified: Thu, 24 Apr 2025 20:08:23 GMT  
		Size: 103.1 MB (103069418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3420f86f4ac4e620281a4fbb2791c00e5c2c56f3d52f777c93f919b82bc9a08c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d8f1bd5dadaaeb87eb9c8e576bf1c5a0996ecd6a740c13040967a001c93912b`

```dockerfile
```

-	Layers:
	-	`sha256:351b8da092897445a129faa58fd40e5d0166dbbbafadcf1f2a22ebc04f89ca50`  
		Last Modified: Thu, 24 Apr 2025 20:08:21 GMT  
		Size: 5.5 MB (5462905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad5fd1dfae910d50c2cadfbc8818c9a6937090a6bdf82e6a6e22a79c942063cb`  
		Last Modified: Thu, 24 Apr 2025 20:08:21 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:279ec27e9f685d64fa7ecfa78d67700f6e369a7173b9e52d601ea180cf2f7191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157028747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d88efbd499d777db050a7e582cf8969d2f43fdf6dec1bd680724d1428e510525`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 01 Apr 2025 20:49:28 GMT
COPY /rootfs/ / # buildkit
# Tue, 01 Apr 2025 20:49:28 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9-1
# Tue, 15 Apr 2025 21:50:45 GMT
ARG package_version=1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9b097260f279cb2efb27736add40063bc2cda05e9ed36312a5fd082e5f79de4`  
		Last Modified: Wed, 16 Apr 2025 00:23:06 GMT  
		Size: 102.1 MB (102067738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fc70f8d2164b17656e8c6809b4323380d8cff8a49f8a5648d7f4a91b1f0ce141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cbcb01f3fbb4e73e9fb018123a85e6dbdf12836a0496f49687779513e527df2`

```dockerfile
```

-	Layers:
	-	`sha256:2da5eed5720b50f0e11d9c473571be9a2a3d92d7ac78b1f8b7bae0f7f698bd4e`  
		Last Modified: Wed, 16 Apr 2025 00:23:03 GMT  
		Size: 5.5 MB (5461719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1394aa35d8aa8fc72c84f898d409cf5301c2b80f7ed80e3b475733fe0d540eb`  
		Last Modified: Wed, 16 Apr 2025 00:23:02 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
