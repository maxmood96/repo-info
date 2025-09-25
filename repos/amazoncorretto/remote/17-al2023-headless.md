## `amazoncorretto:17-al2023-headless`

```console
$ docker pull amazoncorretto@sha256:17a8a46fafc119304f5cdd8d72e6777c42ce46589729877d101662da39531dc8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f9cea9c24b524a1a90d4a5a859173823105a29db72e3aa5ca65cc9b64e98824a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.3 MB (136331280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4524ca2f797d74d4c44dda214428520b7dc13305a1246411216f3d0fd1e7685f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:20 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:20 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:b6baa302384dc877580d7e1080dcca1ed66d9d3b38afc9fcc29c360239e3e362`  
		Last Modified: Tue, 16 Sep 2025 20:50:40 GMT  
		Size: 54.0 MB (54005280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f0634b81ec4f2723afd58140226e355f7712b9ce6061884ce9fbde639afff10`  
		Last Modified: Thu, 25 Sep 2025 02:16:04 GMT  
		Size: 82.3 MB (82326000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b485286db31b49ad77607bdbd56211422469a802c076a4388e436a7fc1329627
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5191563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daf3b1856bb4eb923c85fdc722994896d6f7938b979f7231bc879d890e165384`

```dockerfile
```

-	Layers:
	-	`sha256:9be42326531224302b78b5400157f59623ec069ef802470df70798127013ee6f`  
		Last Modified: Thu, 25 Sep 2025 03:49:23 GMT  
		Size: 5.2 MB (5182816 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29941f6776346389b7ef3968efd89650f3296530944049fd4fcb71e3ce1ea64e`  
		Last Modified: Thu, 25 Sep 2025 03:49:24 GMT  
		Size: 8.7 KB (8747 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9045bee5810ca2542bb7d20af09714a43d3e18db4e5104eb074e8f70e2592473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **134.6 MB (134646956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:573365ae772023b430c9ee5c161709ba553a905c9c6555b495304cf0ca39f5ff`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Sep 2025 20:09:25 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Sep 2025 20:09:25 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8-1
# Wed, 17 Sep 2025 00:23:53 GMT
ARG package_version=1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:202438f011bd656c28426fbd92ff7e7030b77e67ebafd3bec95dbce9626db73c`  
		Last Modified: Tue, 16 Sep 2025 22:16:03 GMT  
		Size: 52.9 MB (52899438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2601fc2d1f4a23b677e8edd48efa9ee20f6f120d8059ca1f8c66e4f22975b195`  
		Last Modified: Wed, 24 Sep 2025 21:13:20 GMT  
		Size: 81.7 MB (81747518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3ebddfaf9e9be0b097c1dcd9d254037e365e2a0434b6c1ea358abede68b65014
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5190435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e530fc36dd27cf4d0f2e4fe83c8d7249921897e8849f7aa79eb769d697de68f0`

```dockerfile
```

-	Layers:
	-	`sha256:66faeaa9f08aa64613dc4cecc01cb529703792a0783ba3b93156a1dc71ff4462`  
		Last Modified: Thu, 25 Sep 2025 03:49:29 GMT  
		Size: 5.2 MB (5181604 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19d3419b4ab705148519824ae09f53af013f5446527e242d2d4ca30431802acd`  
		Last Modified: Thu, 25 Sep 2025 03:49:30 GMT  
		Size: 8.8 KB (8831 bytes)  
		MIME: application/vnd.in-toto+json
