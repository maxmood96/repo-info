## `amazoncorretto:11-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:2003376e655d96e99665635b0e69d2437547a0c902acf91111e0f89456f8becb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d98245f83d9ad564b539f259a4e2ed95283dbeac36b8a278d0ae53c206b2efc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **130.0 MB (130043420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:213210666046be9619e8f1742005c90de79b506e2f8776bdc7e9db57022fb479`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:49 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:49 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:30:56 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:30:56 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:30:56 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:30:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:3ffbc2e8833044834ccfc60c99f6275f3632718226c6ef0c9706b41890795123`  
		Last Modified: Mon, 09 Feb 2026 18:58:55 GMT  
		Size: 54.0 MB (54038228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77af6d0b62da9d44be1bf86f98f3fc96a2f8f72c12d77459d10ba6bb4a55717b`  
		Last Modified: Tue, 10 Feb 2026 18:31:12 GMT  
		Size: 76.0 MB (76005192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:06cd6079ac26a6d1b975d166a3fe3a1f6fdbf9cffca057acea001e25c4671b49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181d590705a635cf4ad5ba21ba96d0354e6daa8c326611e9e407d60bb8df7002`

```dockerfile
```

-	Layers:
	-	`sha256:401a454eb4805c004bb8de322e0cd5a020c1c4fd34900801c135cf58dda4a847`  
		Last Modified: Tue, 10 Feb 2026 18:31:10 GMT  
		Size: 5.2 MB (5196823 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4f474319f98450fe40cd2b4d6367dba2e442c272af784e2cb4f429ccddefd935`  
		Last Modified: Tue, 10 Feb 2026 18:31:10 GMT  
		Size: 8.6 KB (8609 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5f9dc03c08659dc5a240dc879a4b22f69f594acf27a5c21589947a572d15900
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **128.2 MB (128156505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad4aa9112c5b96c1b9e2abd9cbdebfafc0816f55a7ecc52eb3eab2b249d17a98`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 10 Feb 2026 18:13:36 GMT
COPY /rootfs/ / # buildkit
# Tue, 10 Feb 2026 18:13:36 GMT
CMD ["/bin/bash"]
# Tue, 10 Feb 2026 18:31:01 GMT
ARG version=11.0.30.7-1
# Tue, 10 Feb 2026 18:31:01 GMT
# ARGS: version=11.0.30.7-1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2023.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-11-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Tue, 10 Feb 2026 18:31:01 GMT
ENV LANG=C.UTF-8
# Tue, 10 Feb 2026 18:31:01 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:72831a4cffd207c00f002b53208af67cc59cf3af51b98b118c11c230a7926a2d`  
		Last Modified: Mon, 09 Feb 2026 20:01:25 GMT  
		Size: 52.9 MB (52918211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea486ccd732bb993e26049a70e04b700eeaef59b71e2f9ee2b06d7cc8b36fb4d`  
		Last Modified: Tue, 10 Feb 2026 18:31:18 GMT  
		Size: 75.2 MB (75238294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2343c5f10ce0d5b2e8e4614687edc89364762ebca244017c8c9c5ce34b4ddecb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5205130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a62d1baa5e8d04c48f8c9e41da77ba5f5e2a2cfd9883cb0a6c501331f8e07e`

```dockerfile
```

-	Layers:
	-	`sha256:01bb4fdfed961cbf8ef48f9b5ee1960f1327313400d4b708068ed268c91575a7`  
		Last Modified: Tue, 10 Feb 2026 18:31:16 GMT  
		Size: 5.2 MB (5196441 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05dceb5ae52266816344ad8a67716d0a250388d8298724e857346d020638d722`  
		Last Modified: Tue, 10 Feb 2026 18:31:16 GMT  
		Size: 8.7 KB (8689 bytes)  
		MIME: application/vnd.in-toto+json
