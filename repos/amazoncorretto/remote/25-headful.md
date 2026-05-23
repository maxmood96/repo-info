## `amazoncorretto:25-headful`

```console
$ docker pull amazoncorretto@sha256:2a734a9384c0491c16c30a55cce8832ed488203f2428eddc346e31b4775e52b9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cf6336b13c6da8265ab9ba1a8404be40685b13083d9914f0d49bca9afc2e0e9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159012376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2703a2d88ee24703c8998d48f525b068c3ec33f55ac1507e38239398ce232667`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:06 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:06 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:41 GMT
ARG version=25.0.3.9-1
# Fri, 22 May 2026 21:12:41 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:41 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:41 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:c00ef2b893da480d77c559b6862d1ad542cc91c6bb2d3106a00cb8d9c141b797`  
		Last Modified: Fri, 15 May 2026 20:34:40 GMT  
		Size: 54.6 MB (54572440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3761b51f2ee9212a151854626cc1fa9dfe85070069879c31cc3286e40a6fa834`  
		Last Modified: Fri, 22 May 2026 21:13:00 GMT  
		Size: 104.4 MB (104439936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:95b3eb6337c1a68ecf69fcd1bf862d1d757321a4a967e129aac68dccb4cbcc67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fec47e751f419e4368125175076a47a375ec4ec118a706a30c1d9f1a8d19001b`

```dockerfile
```

-	Layers:
	-	`sha256:699c3f8a8b62951a28984aecef738d17b4848b0907d288b343d09c7c8ecd2748`  
		Last Modified: Fri, 22 May 2026 21:12:58 GMT  
		Size: 5.2 MB (5227475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e4e882def32897586b7044d63de26b3a16bb38fd6c6905ab218cb6ad1500dcc`  
		Last Modified: Fri, 22 May 2026 21:12:57 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9904251378626b05200530a1529c3dcb30e0ccbc23a78de9a24ce338407ad102
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.8 MB (156843959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d507ed05c66760a3161f41cd2de5023478f460d45aa12bd9c2dea1221f3ca1`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 22 May 2026 20:12:25 GMT
COPY /rootfs/ / # buildkit
# Fri, 22 May 2026 20:12:25 GMT
CMD ["/bin/bash"]
# Fri, 22 May 2026 21:12:21 GMT
ARG version=25.0.3.9-1
# Fri, 22 May 2026 21:12:21 GMT
ARG package_version=1
# Fri, 22 May 2026 21:12:21 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 22 May 2026 21:12:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 21:12:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:a92e5e4b9e90f970dfdf3c3258e673bb767c6401beba9985a3b635162466eedd`  
		Last Modified: Fri, 15 May 2026 20:34:37 GMT  
		Size: 53.5 MB (53454415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5537baf1d388b4e50ed6c91c9ab5070d0aefda34693e17c592dff078f87252ab`  
		Last Modified: Fri, 22 May 2026 21:12:42 GMT  
		Size: 103.4 MB (103389544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f017cabfc2a6f790ed01c43e01bcd7da7dad22ab6adef71621f4b8c0f14198f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3847fe19d9a20a632a22148d90c6c6774b8891721b496cd7dcb82a456c3fde`

```dockerfile
```

-	Layers:
	-	`sha256:fbc9bf197c65d88354136460adcc9ebd0c46d60dcc8594a35f32ec7e423e9364`  
		Last Modified: Fri, 22 May 2026 21:12:39 GMT  
		Size: 5.2 MB (5226290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6cbd4b2955a7a0a435b5f7ae0a45a997e296b8908466cae762fe85b4dfb39352`  
		Last Modified: Fri, 22 May 2026 21:12:39 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
