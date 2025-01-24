## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:293e26386631b1dccd0151f87a45c7466f941a3bba587aefd2cdf2547a67186a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2126ae0c9738c809065cacf39a6eb1201db0cb725d763025863ad54119e4221f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.1 MB (150054159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c960f4b2917f18d4a424d9d0a4f063b89f717b01cbc81c42276c8a86b10b505f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:39 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:39 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2ddc0aa2636ed19b988b4176374929a92f5862f6c6e88ea255d352140af781e6`  
		Last Modified: Fri, 17 Jan 2025 20:13:56 GMT  
		Size: 62.6 MB (62648554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3a9a7793ebaddb8501ed5e54a46d391a32f45aae2f46a7bbcfadfbbb3a374e`  
		Last Modified: Thu, 23 Jan 2025 23:08:18 GMT  
		Size: 87.4 MB (87405605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2bb49f0b686ddc4f3a5d9f3c4231e512b89502addde1c0b25cb8f624aeb671cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56593df6c50a44bef7da4278ab363bbeb9e69c263444e64e1f19dbcfc84d24f2`

```dockerfile
```

-	Layers:
	-	`sha256:b3a976bd7462df255b185b816b9b1271e8e821434da656cfe2fca73b2f8fd483`  
		Last Modified: Thu, 23 Jan 2025 23:08:16 GMT  
		Size: 5.6 MB (5615849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ac1d0f44222cd7a639d5a690f096d0c74cdea25d5b7830204888aed674eb98`  
		Last Modified: Thu, 23 Jan 2025 23:08:16 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:06c00643cff4f2c067dedc49c37d352a1b024a737b48e7719b602541fad5b2bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144299210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:045c87f20232887bec0a5d6e500592f29284b25c30d1e1c5cdc234b4acacce7b`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 17 Jan 2025 22:08:43 GMT
COPY /rootfs/ / # buildkit
# Fri, 17 Jan 2025 22:08:43 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:dc3d403853487343f06bffefe21e65d842f88da2d7a1073ba2820fdb1b7ece72`  
		Last Modified: Fri, 17 Jan 2025 20:14:11 GMT  
		Size: 64.6 MB (64590432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b05a52bb7540d9d841bc10ac0a17792148c22ba2f9a5fca84b4326f22ef9e78`  
		Last Modified: Thu, 23 Jan 2025 23:19:49 GMT  
		Size: 79.7 MB (79708778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3d9e523d3add11365af5c4b6ec0e15ffc436ede14de451eef735d4961ef5ca7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3c8800b4bcbb32b9553419c83d91fff09068b8b33423790e415eeb3b0e746aa`

```dockerfile
```

-	Layers:
	-	`sha256:3a35d180d47cb321ca4b5eb0f6bcb5bb190b90ca8b79a8a96dbc4ee51cd2f06b`  
		Last Modified: Thu, 23 Jan 2025 23:19:48 GMT  
		Size: 5.4 MB (5432125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bdaf45bb34110896f0a6fc85285310403d21ce4440bf44ad6bfb3bb7ec3434a9`  
		Last Modified: Thu, 23 Jan 2025 23:19:48 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json
