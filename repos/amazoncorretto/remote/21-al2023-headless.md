## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:21d77c7ce46b1e3f0257bef3e3487c1e5ca3ae1626629ae45b59111b28bd88b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3e7fe18477a91b796bc400dd4143de74e04acf72e2587ca3eea9d76b28a2eec8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.8 MB (141837333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f4b542caa6b26214fe541cd5d96998ce0cfe9238356f1643c706925450098`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:21:43 GMT
COPY dir:78fa4f6b1d2d2862367cf50eabd290fdf95c6fac76e06e7e2e34c2d4247bf889 in / 
# Fri, 05 Apr 2024 18:21:43 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 19:30:35 GMT
ARG version=21.0.2.14-1
# Fri, 05 Apr 2024 19:30:35 GMT
ARG package_version=1
# Fri, 05 Apr 2024 19:31:21 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 19:31:21 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 19:31:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:81e74100301dffd9fca7e4378ed7aecb21d613798689a5481ed8365657bf5efc`  
		Last Modified: Wed, 03 Apr 2024 01:55:13 GMT  
		Size: 52.3 MB (52323905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:381c9da2b7d2a864214a1ee8875afa0952dc41bbe6bc8639df9381ea3d92c4f7`  
		Last Modified: Fri, 05 Apr 2024 19:43:23 GMT  
		Size: 89.5 MB (89513428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0782ac354f105ea5cf014786f301e8174aa1abbae10950045463e5f97dc57a7d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.0 MB (139978881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4575876f5b7540e2b1dfa210cfc704a9f93999b7ef79857177f0a8f3df329840`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 05 Apr 2024 18:07:15 GMT
COPY dir:f8d39fbbd7bf18543727aab8c7ebde8152233a1cedabf00f365356d7779f0166 in / 
# Fri, 05 Apr 2024 18:07:15 GMT
CMD ["/bin/bash"]
# Fri, 05 Apr 2024 18:51:18 GMT
ARG version=21.0.2.14-1
# Fri, 05 Apr 2024 18:51:18 GMT
ARG package_version=1
# Fri, 05 Apr 2024 18:52:01 GMT
# ARGS: package_version=1 version=21.0.2.14-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf
# Fri, 05 Apr 2024 18:52:02 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 18:52:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:2db99c85d8118887d64b46dad6e559ea58c1ef5620f9a766cd0658af1ec030d3`  
		Last Modified: Wed, 03 Apr 2024 02:28:44 GMT  
		Size: 51.4 MB (51408325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c83f1d5369addd8e319cabd57a31955eeba30193e69242a1c0c6f048a218c76`  
		Last Modified: Fri, 05 Apr 2024 19:02:16 GMT  
		Size: 88.6 MB (88570556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
