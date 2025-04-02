## `amazoncorretto:17-al2023-headful`

```console
$ docker pull amazoncorretto@sha256:2bf98d525421cd8bc755cc3eb159bbdd34ccb1ab5273e68005f7d14e1d682a31
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2023-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:184d5ae03a50ee07bc4c8b78e02f9811df8a8e262a82fb2341f0941383f5bf6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **138.9 MB (138856428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ef7164fe2a43a1ae48836568a571cfd0f881bb46070ff2f2f41451108139d6`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:a60da04a601b8a4165b40817da07cd2d6e94c2b008c87988152b943d6465d10c`  
		Last Modified: Tue, 01 Apr 2025 23:53:54 GMT  
		Size: 55.9 MB (55907053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28c4136f829226f1ef734b6a7901fdc2969a69ff47073f849729f367a233aebd`  
		Last Modified: Wed, 02 Apr 2025 00:00:21 GMT  
		Size: 82.9 MB (82949375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:44cfae70ebf26398d8020a87568f58d5b41da1aa9f295a79eba54390e4e486ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862a0c9335d4d7f876ce7ebaf690a2f00214864ddcecff0580ae72603dfb1f10`

```dockerfile
```

-	Layers:
	-	`sha256:3ce40053f2d813fa7993dfbd0ba5aa0511fc8aaef89c47c6cb1dfb390713bd3f`  
		Last Modified: Wed, 02 Apr 2025 00:00:20 GMT  
		Size: 5.5 MB (5451028 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e49ff1d9497253d4813182d62e3b8e056d118c69bad59ca683864c59c66cbbdd`  
		Last Modified: Wed, 02 Apr 2025 00:00:20 GMT  
		Size: 8.9 KB (8934 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2023-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7fcb79a2d52aa0cc8f016b9bd9b0278a23cc6f3567ac9eaa5cddf804e7b94e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **137.4 MB (137352286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b563156fd1430665e561e05b0c71f6e8f7d93c63fbc4ccbb98a9d92d04761909`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 21 Mar 2025 22:11:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
CMD ["/bin/bash"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=17.0.14.7-1
# Fri, 21 Mar 2025 22:11:14 GMT
ARG package_version=1
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=17.0.14.7-1 package_version=1
RUN set -eux     && rpm --import file:///etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2023     && echo "localpkg_gpgcheck=1" >> /etc/dnf/dnf.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2023.${package_version}.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2023.${package_version}.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/$(echo $version | tr '-' '.')/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: digests signatures OK" || exit 1;     done     && dnf install -y ${CORRETO_TEMP}/*.rpm     && popd     && rm -rf /usr/lib/jvm/java-17-amazon-corretto.$(uname -m)/lib/src.zip     && rm -rf ${CORRETO_TEMP}     && dnf clean all     && sed -i '/localpkg_gpgcheck=1/d' /etc/dnf/dnf.conf # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7143537c6705cbbbdbc85156f432de0957d3f1d609224d7a95b58e33cc7549dc`  
		Last Modified: Tue, 01 Apr 2025 23:53:38 GMT  
		Size: 55.0 MB (54961009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8978a72aca98d7cc4ba24d6ec8824415fb8a486adf0c16f0388fde8dd6797e2c`  
		Last Modified: Wed, 02 Apr 2025 00:32:18 GMT  
		Size: 82.4 MB (82391277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2023-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5e44067654f75095c68051fe767d402d32c395f2d09f8c36031ebb045cb6c06f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5458833 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42bdd6c1c26b29815680db764377bcdf1e1b4f590bb814f76c2535d8724643b7`

```dockerfile
```

-	Layers:
	-	`sha256:883fb71596c620aff8a419d525d9d333a9fc920f3919ab8b862eb2cea5f38ed3`  
		Last Modified: Wed, 02 Apr 2025 00:32:16 GMT  
		Size: 5.4 MB (5449819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0c14f8e7583b2b23f7a54e0be9d627008d869d24849f1544169f953d3e818c5`  
		Last Modified: Wed, 02 Apr 2025 00:32:15 GMT  
		Size: 9.0 KB (9014 bytes)  
		MIME: application/vnd.in-toto+json
