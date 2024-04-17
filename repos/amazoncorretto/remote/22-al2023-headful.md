## `amazoncorretto:22-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:90cbffd36fdf1e765628c6c64fdbb142628015473e23ec855240d209b1d3c1ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:006819ba806bda4b89fc6ee15ebfe47e6b03a6cbdbaf893c6a3e500988b92d5a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.6 MB (141638949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd12f614588a2efd515e88b03e781b424e6b2e379295f98588035070552f4cd7`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:06:41 GMT
ARG version=22.0.1.8-1
# Wed, 17 Apr 2024 00:06:42 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:07:48 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:07:49 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:07:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71b0285ac184809ca095f2ecb077870e1030d5c7de944ddaf5f1b81ab142ad4a`  
		Last Modified: Wed, 17 Apr 2024 00:27:58 GMT  
		Size: 89.3 MB (89315044 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d976f7517789f7769ffb03c32f94e63c4b3dcd5437515359dfeca6b73113dff4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **139.7 MB (139689928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa13d6ca68fe87e4fe09184bc29b24a343d9fa44d9ed1ebbbeaf41076049550`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Wed, 17 Apr 2024 00:15:39 GMT
ARG version=22.0.1.8-1
# Wed, 17 Apr 2024 00:15:39 GMT
ARG package_version=1
# Wed, 17 Apr 2024 00:16:39 GMT
# ARGS: package_version=1 version=22.0.1.8-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-22-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-22-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-22-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Wed, 17 Apr 2024 00:16:40 GMT
ENV LANG=C.UTF-8
# Wed, 17 Apr 2024 00:16:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-22-amazon-corretto
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b60f0c1ceba110a3f5ad775c81b7688089dd36d870a68914b23cc9fb4b5bfec`  
		Last Modified: Wed, 17 Apr 2024 00:36:50 GMT  
		Size: 88.3 MB (88281603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
