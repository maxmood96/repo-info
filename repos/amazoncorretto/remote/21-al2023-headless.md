## `amazoncorretto:21-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:fd2ead88421b93b904cf7ebcf43b073b165fa84d58b1248424a90e41675f8a22
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16b14c0b22327700105cb7213eb54e142e53cbe54968b1f1f456ea22f5510a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143276851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04634b3f101800020cabcd6666be26091c6badd865a3a864ce168079019c7a9e`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:05 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:32:05 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:05 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:05 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c2072167316556997df7d620b00f650d07a6429e7050821eba1ba66429c6c5`  
		Last Modified: Tue, 10 Feb 2026 18:32:23 GMT  
		Size: 89.2 MB (89238623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de35d7eb6d40aa97aacd40d065ead40aa6b052f9b7f8b0e5c87b1578e3b6c7a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5193230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44abf34669457f80b181ba251f2f178d6ea7bac37223ac7d2aab3b55e7972027`

```dockerfile
```

-	Layers:
	-	`sha256:d2b9ff2470f22aa9c5be06c2391e69314c49bad905b81a4412764a9ee2032803`  
		Last Modified: Tue, 10 Feb 2026 18:32:21 GMT  
		Size: 5.2 MB (5184522 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c301a3e9c95a3451d01df21d102604ffb133f78e901606c21281058a897bcd92`  
		Last Modified: Tue, 10 Feb 2026 18:32:20 GMT  
		Size: 8.7 KB (8708 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:15b7c06f7245ae1ba3742fdb1884a1157391130aab359a6405e7082124c647b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **141.3 MB (141289279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f68a6b063b93d78cf23be233e1d91175fb3e64a3832bd44c69a5c7f49bb5071`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:32:06 GMT
ARG version=21.0.10.7-1
# Tue, 10 Feb 2026 18:32:06 GMT
ARG package_version=1
# Tue, 10 Feb 2026 18:32:06 GMT
# ARGS: version=21.0.10.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-21-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-21-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:32:06 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:32:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-21-amazon-corretto
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e534712815e2100f25aaca9c2d1fe0cd794da23c0e56a66e03c96765688c966`  
		Last Modified: Tue, 10 Feb 2026 18:32:24 GMT  
		Size: 88.4 MB (88371068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ff5e3e366bcfe60fadd870665b24b1ad9229e8b1ed9dc485f13b5bab90b5f3d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5192100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36d2fffefb3459c9bbe60e2e4c22507e73ba8d120bb7d5144422345047c23de`

```dockerfile
```

-	Layers:
	-	`sha256:ea5af99c71ccf4147cc103c91327f209421852a07fdd5222940a992e82d28803`  
		Last Modified: Tue, 10 Feb 2026 18:32:22 GMT  
		Size: 5.2 MB (5183312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26eb6a2b2ead37c13f2c22a88122195b4d502fd55d4b5c718f449d22c86d9af7`  
		Last Modified: Tue, 10 Feb 2026 18:32:22 GMT  
		Size: 8.8 KB (8788 bytes)  
		MIME: application/vnd.in-toto+json
