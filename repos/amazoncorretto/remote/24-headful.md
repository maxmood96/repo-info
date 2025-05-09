## `amazoncorretto:24-headful`

```console
$ docker pull amazoncorretto@sha256:65a2b5b16cd01c6599f4419e9f018e93323218c9f44656797fcb96114e848843
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-headful` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4f080f0be5d584ebe5a2e543189091986e1a8754272cfce9b2cc690279dc8f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.9 MB (156877440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a3a669b3a0edb773a25832cffc87e780e98225d827355dac619e041f0949408`
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
	-	`sha256:1c3112c87ab2d6209030c22629180b5d1958fca3765b3cbcfbc9bcfa1ee6e425`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 53.9 MB (53880920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ac166cf3d05d53f6115bdd75ca33659bf4ccff93a6a11c6c473b615dc85ce4`  
		Last Modified: Thu, 01 May 2025 21:08:21 GMT  
		Size: 103.0 MB (102996520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b8970529b288ced2bec8d4c1e8fc9fd553dc0f0835f2b626f954a9ddf7392946
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5214644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba2cabdc7e186fc0018ecb003ec4b398f10deb0d792443ace1e572d6240a16af`

```dockerfile
```

-	Layers:
	-	`sha256:9d3ed9f860d025da65dfbda42279eb6ab5a753b29f66621302e0813d2c130237`  
		Last Modified: Thu, 01 May 2025 21:08:20 GMT  
		Size: 5.2 MB (5205394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e118f1e5185512ab5943600a67f90bf687b9a9081376ca266fef965962408876`  
		Last Modified: Thu, 01 May 2025 21:08:20 GMT  
		Size: 9.2 KB (9250 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-headful` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:667656a00853176c3a5acc2828d4e7e09baf91ff2a0911224456070637b83bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **154.8 MB (154809060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cff0292d7c6c01ec4d57bf16c6c603b014884ca7b838d1010603b8083c23799`
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
	-	`sha256:5804bd91a568b15c202af6e01f57d869865af0d532f8773d8faefb503ef0bbfe`  
		Last Modified: Thu, 01 May 2025 02:47:15 GMT  
		Size: 52.8 MB (52811047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5236ee57928cf3e52bd17ffc7b27798c23abb52a834535d59e5103c4ff812a`  
		Last Modified: Thu, 01 May 2025 21:26:59 GMT  
		Size: 102.0 MB (101998013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-headful` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7259e94727af0dec73b507d46d5d2ad2d208d28f45fcf9a30b53057e8eb0811a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5213550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44d77305758884fe656f950e6d3381b925c07bbf51f0b20bfa3264fb6f34bc7`

```dockerfile
```

-	Layers:
	-	`sha256:dda66cf2986eb752ffa512e58b2b549337177f4172002bcbe12a38db11d834f8`  
		Last Modified: Thu, 01 May 2025 21:26:56 GMT  
		Size: 5.2 MB (5204208 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7134e66a19c44234145886bc8286e12c1f8d0d7e12becff259d685ec7e411a39`  
		Last Modified: Thu, 01 May 2025 21:26:56 GMT  
		Size: 9.3 KB (9342 bytes)  
		MIME: application/vnd.in-toto+json
