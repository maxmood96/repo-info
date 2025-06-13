## `amazoncorretto:24-jdk`

```console
$ docker pull amazoncorretto@sha256:14a840c3f5b75f86ff640a785dcc875d0b33453abe94854a55f6d1e17d7c3b88
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:55d294935e92faf4b12e7aa0c2495663da80992729242f42e3f9a845f083ff90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **240.8 MB (240763131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd580064eb545df61ce428e231219be0bb6e5cebe1a57b0c9d3f448bd59d0cfd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:b32084d69388d1a83137a801da01717a35f31eef39012331796a50e2c2385667`  
		Last Modified: Wed, 11 Jun 2025 22:05:56 GMT  
		Size: 53.6 MB (53570360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec66c391cf9a3d196d14d11e9af9cf5afbdc77df45f01f053c094f4c9c106d6`  
		Last Modified: Fri, 13 Jun 2025 17:12:58 GMT  
		Size: 187.2 MB (187192771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a41819da1c61542a79ab9919fee1c612cf145b84578f26b9198a630ac09b20b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5340106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee23acaa217731b182344b2c55a62cbe6a2464d561a1588deb34ac4e347396a7`

```dockerfile
```

-	Layers:
	-	`sha256:81bea908a2d63186f3d661c6e8380c5244deaaeef73f0302550bb69570fbddfa`  
		Last Modified: Fri, 13 Jun 2025 18:49:18 GMT  
		Size: 5.3 MB (5329869 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7687792274a00399bdd76d41b382fd50ca89bb2d1a9ca0a5c8bfba065159ed19`  
		Last Modified: Fri, 13 Jun 2025 18:49:19 GMT  
		Size: 10.2 KB (10237 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8f781c842287837928fd0b402573fcff666c5d0cdf3f82cd11df8d0bd01ff949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **237.8 MB (237798629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a51a642977776ff04b45274ffd24a776ac2e5fdf8212b3399fe6a45d82db63d2`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 09 May 2025 18:18:04 GMT
COPY /rootfs/ / # buildkit
# Fri, 09 May 2025 18:18:04 GMT
CMD ["/bin/bash"]
# Fri, 09 May 2025 18:18:04 GMT
ARG version=24.0.1.9-1
# Fri, 09 May 2025 18:18:04 GMT
ARG package_version=1
# Fri, 09 May 2025 18:18:04 GMT
# ARGS: version=24.0.1.9-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-24-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-devel-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-24-amazon-corretto-jmods-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-24-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 09 May 2025 18:18:04 GMT
ENV LANG=C.UTF-8
# Fri, 09 May 2025 18:18:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-24-amazon-corretto
```

-	Layers:
	-	`sha256:b9b2e8e61af6809d54a17702fba1fe6b09b2947a739f90536e2d0bb6a4ed34cb`  
		Last Modified: Thu, 15 May 2025 19:36:48 GMT  
		Size: 52.6 MB (52565737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8606c71bde4a7d05e0626f9b64fb3e0bc776c63157501c509a656a16ad481691`  
		Last Modified: Tue, 20 May 2025 07:19:50 GMT  
		Size: 185.2 MB (185232892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ea0dbd10d8418f20d63bdd177cee3a129edff9f2339af23366157e029943933
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5336177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8cd77f1c6d05511dd1937ef99aa4e0d9868407dbc9a4fd903ce35b610a6e863`

```dockerfile
```

-	Layers:
	-	`sha256:9534069b2d449dc1b5da509da6a17fcb217a4017acdbc19d37fb2fdcdc037ee4`  
		Last Modified: Tue, 20 May 2025 00:50:05 GMT  
		Size: 5.3 MB (5325823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73546b898a809cc82c36bb02415562ce76a5ffb9b058a5f3e9ad32dcb0acd81e`  
		Last Modified: Tue, 20 May 2025 00:50:05 GMT  
		Size: 10.4 KB (10354 bytes)  
		MIME: application/vnd.in-toto+json
