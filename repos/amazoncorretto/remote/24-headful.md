## `amazoncorretto:24-headful`

```console
$ docker pull amazoncorretto@sha256:4cae4ee58ca8b04760bb9ebba2ad26c668a5243a4bc27fc3a30d1971377c94e0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headful` - linux; amd64

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

### `amazoncorretto:24-headful` - unknown; unknown

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

### `amazoncorretto:24-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:71d2eac427e8346611bda8b118f549921637cc75e327ad1d98ae9173b6b4adeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.0 MB (157029397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:647e221aeabd5795b89e64868489c524c2f996402e5c48117a1455560ab53de4`
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
	-	`sha256:3851c1e87439f4d250c3c0908923968a64dd743e1e5cfc05b798a52dc5d1e215`  
		Last Modified: Thu, 17 Apr 2025 22:49:07 GMT  
		Size: 55.0 MB (54961479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce6912b18726f5e9445b1994793934ca3757f3a263dea4d929aea43aa5b9a93b`  
		Last Modified: Thu, 24 Apr 2025 21:26:24 GMT  
		Size: 102.1 MB (102067918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:92485d24313aac783fe07726456095329956d0e3ff3d7af708d1a689f6f03c24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5471060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62e6bc16978185a161f45560aacd0cef979ff1b89300d0053db2c05b5eedc3ce`

```dockerfile
```

-	Layers:
	-	`sha256:80223e6a77e773da70e403a671af8e194ea8024fce6d880afa0a5b82202a18e4`  
		Last Modified: Thu, 24 Apr 2025 21:26:21 GMT  
		Size: 5.5 MB (5461719 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f1cf7a4739f6759adcf8ad22cfb583bcfe395690c75255cab425533e5b14e20c`  
		Last Modified: Thu, 24 Apr 2025 21:26:21 GMT  
		Size: 9.3 KB (9341 bytes)  
		MIME: application/vnd.in-toto+json
