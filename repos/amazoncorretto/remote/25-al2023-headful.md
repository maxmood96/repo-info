## `amazoncorretto:25-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:6f6446401ff8f205c7c54e85ea5f84675b5781692a46d7d88c0040cd7c8ff0cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bc7283c7c46edef1723165a23ee64e48064c6c968c2a6e11c4deabedfe079dd2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.0 MB (159015007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35092e7d8581d8b8d441f03dd4f3d510f59167eb8e368de38c12a94533c93a44`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:38:48 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:38:48 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:13:11 GMT
ARG version=25.0.3.9-1
# Mon, 04 May 2026 20:13:11 GMT
ARG package_version=1
# Mon, 04 May 2026 20:13:11 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:13:11 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:13:11 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:1b0df00d658b743fe77f94b0de8f604514c4bff7937f6920366cc51ff5527b94`  
		Last Modified: Fri, 01 May 2026 01:37:32 GMT  
		Size: 54.6 MB (54576753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16a8925b224d5ed49ef8b2486124b805b7dbb187529cf30482714d8d7df7502b`  
		Last Modified: Mon, 04 May 2026 20:13:34 GMT  
		Size: 104.4 MB (104438254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:76392a872a5f474e1a3e7532538dc31842bed359bd7ed6d107996dacead5bd90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5236843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b42bd0eb22fb8adceaf60076fbdb4d5a719478441803938bc0b955e963fbb2c8`

```dockerfile
```

-	Layers:
	-	`sha256:63c11a627d161fd14f8b69424080387c74236de98d2f24f7ec01309f0b5b390f`  
		Last Modified: Mon, 04 May 2026 20:13:29 GMT  
		Size: 5.2 MB (5227475 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:baf2623a7ee83572b24ac121f6bc07e82789f05c33225f2442ebeaa9ff9e94fd`  
		Last Modified: Mon, 04 May 2026 20:13:29 GMT  
		Size: 9.4 KB (9368 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:df7f98554c0a44981f08ceaa66b4d9a25e44561598f646dbb033054b8499ad9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156850016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca74f016cb7b7cb0d799a03264658c1a7a9210cea13cf649cd6d1cf48b9aef40`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 04 May 2026 19:40:10 GMT
COPY /rootfs/ / # buildkit
# Mon, 04 May 2026 19:40:10 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2026 20:12:40 GMT
ARG version=25.0.3.9-1
# Mon, 04 May 2026 20:12:40 GMT
ARG package_version=1
# Mon, 04 May 2026 20:12:40 GMT
# ARGS: version=25.0.3.9-1 package_version=1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-25-amazon-corretto-headless-$version.amzn2023.${package_version}.${ARCH}.rpm" "java-25-amazon-corretto-$version.amzn2023.${package_version}.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-25-amazon-corretto.${ARCH}/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Mon, 04 May 2026 20:12:40 GMT
ENV LANG=C.UTF-8
# Mon, 04 May 2026 20:12:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-25-amazon-corretto
```

-	Layers:
	-	`sha256:72d58419c7ebc63fc61c6dea23f165375b7ce301be1edaba1ce1a38a9af5352f`  
		Last Modified: Fri, 01 May 2026 02:58:16 GMT  
		Size: 53.5 MB (53456770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6e682447975023a07e06bf4d088c3def169308dc192217e7da7b87d597f19b`  
		Last Modified: Mon, 04 May 2026 20:13:02 GMT  
		Size: 103.4 MB (103393246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e3eca8fadf86fb5aa39851580b3e2f125229cfd1edd3f073c6f6f8c8c52abb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5235749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396940737b832e608a32ff6a73aa4f64ec707eedfea214eaba1d5c94b6a4c06d`

```dockerfile
```

-	Layers:
	-	`sha256:a1827ef030bc0291cbf84f6416a460c73033e67c256918e5b518e784ee836855`  
		Last Modified: Mon, 04 May 2026 20:12:59 GMT  
		Size: 5.2 MB (5226290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:89db3e97199b04db0dfe85a45d91986118c3978fcf0e1d0e60f33756fb66df24`  
		Last Modified: Mon, 04 May 2026 20:12:59 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
