## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:2db5926776297fe80708f9bd8f763f56e809b792375a3843d9b4cf408b8ea98c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ff9df840104dca71d37efe4d54dd5798019ebd8373ba1e3d4d01fea7976e8692
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.7 MB (228679138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:552d42103ea45b22ae3227fbfc88399025ab59be243a36643e3997eff1e70e31`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:16 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:16 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:59 GMT
ARG version=17.0.17.10-1
# Thu, 15 Jan 2026 22:09:59 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 15 Jan 2026 22:09:59 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:89d3b5863331d6bb79d550bf0acce60aeac36e2c065470bf6d6f8d76c9cb6f4f`  
		Last Modified: Wed, 14 Jan 2026 13:13:55 GMT  
		Size: 62.9 MB (62940156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4018cbc2580931c956cd745a221cac3d7f9f9d3bce9c5f4e322552f8d3fc3cd7`  
		Last Modified: Thu, 15 Jan 2026 22:10:44 GMT  
		Size: 165.7 MB (165738982 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:82fac3cd6b0da0319e12ecbcdbc9b40572895e5fca2a0cee858be07e44c8bee3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5981743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa9ca906629902deb82f9fb0424d367b3deb5e075cb32df93d9e15c532f4d60e`

```dockerfile
```

-	Layers:
	-	`sha256:487d7a16cd51c2d027494fafc328b531d4faa65f8ac842d0d350584fdca6cf55`  
		Last Modified: Thu, 15 Jan 2026 22:10:18 GMT  
		Size: 6.0 MB (5971824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ceb7952854e68f044798bef976a13dea22f85ad1fe05bde8e03e9d75b4c108e3`  
		Last Modified: Thu, 15 Jan 2026 22:49:45 GMT  
		Size: 9.9 KB (9919 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:089c017a029e8698789e5c8a9b76751b184c86e896e148d02147f31d77427709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.0 MB (221043685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86717a248a8586047bb904f162ccd95a9dcc8a7cd4ee5b80beb08169e588a1a`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 15 Jan 2026 21:44:03 GMT
COPY /rootfs/ / # buildkit
# Thu, 15 Jan 2026 21:44:03 GMT
CMD ["/bin/bash"]
# Thu, 15 Jan 2026 22:09:41 GMT
ARG version=17.0.17.10-1
# Thu, 15 Jan 2026 22:09:41 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.$(uname -m).rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 15 Jan 2026 22:09:41 GMT
ENV LANG=C.UTF-8
# Thu, 15 Jan 2026 22:09:41 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:afb133ffe3cfc9458fcd28fa75abd002d894e187faa842d48d3c35c676633646`  
		Last Modified: Thu, 15 Jan 2026 18:33:41 GMT  
		Size: 64.8 MB (64770434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30928d753f5c5781b4d61d6a43dc494110eb63cf6a1c366a9d881185a7e1c82`  
		Last Modified: Thu, 15 Jan 2026 22:10:03 GMT  
		Size: 156.3 MB (156273251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:42135c579602a0057cc6e765bb9337027e327e0e2ec53c9e0ea23c467f68c4aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5773693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7d8fe87487c3a3d5944f56f54d7076adb0ea668fcb3e958ea2fc11ab2fa6174`

```dockerfile
```

-	Layers:
	-	`sha256:0c8d155b9c594c4cf7ae87f4b6fd332e13ed85169c34f0d7dd37adb12fea438d`  
		Last Modified: Thu, 15 Jan 2026 22:49:53 GMT  
		Size: 5.8 MB (5763694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:178f98ea22ba1dde862aee07a4f70647f3e50e4dba5d50ada5a670f483446a28`  
		Last Modified: Thu, 15 Jan 2026 22:49:53 GMT  
		Size: 10.0 KB (9999 bytes)  
		MIME: application/vnd.in-toto+json
