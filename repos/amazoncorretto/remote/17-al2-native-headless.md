## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:bb75caee9d0fa0c2ca84a27eda348eb1df772c05839e6eccdb0cc79c80fa224f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:be578d4a879b6f4e1e79901d7e5f4996897daeb6c78f432994e971bf30cef513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.2 MB (150248462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4b3961daac4c8d31caafa426cc55f181b3e49887dd3d509cc049ccb83e22ffe`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:37 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:37 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:68b5eef1eb563a36e20df422ee1592c70689019fdd12cc4fdc4e4b24c31c1c77`  
		Last Modified: Thu, 27 Mar 2025 19:19:22 GMT  
		Size: 62.8 MB (62752889 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8a7a1a02f6baa58d54cc2977966d81d94163d96fd9f7ba66982c9adf8b1710f`  
		Last Modified: Tue, 15 Apr 2025 23:55:57 GMT  
		Size: 87.5 MB (87495573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da6cd6fa29fb3ca471016074bd7a6e9549d2dc97f70bf72ae7dd2c0d96e0f8bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0910ac9d5cdadb3571e43d39284afdcc080caa82065d157e99625c04257aa700`

```dockerfile
```

-	Layers:
	-	`sha256:e3aed07275e8a3ed8719f516e5aa1469c1a523450c6234dc7400d8b7fa198225`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 5.6 MB (5615877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a872dee3b01b8fb337b5119162135da8b81da726b839d09681d11af3957ce123`  
		Last Modified: Tue, 15 Apr 2025 23:55:56 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a7ccdb5a65342c0aa71425d81a0398038aff85fc52656608b499aa9c2fe066e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144303680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5af4e5ad62092f0985c2641a64c72a73a1f0bd6bf2d1c8159a31e9ab48a5d627`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 27 Mar 2025 17:58:42 GMT
COPY /rootfs/ / # buildkit
# Thu, 27 Mar 2025 17:58:42 GMT
CMD ["/bin/bash"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=17.0.15.6-1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=17.0.15.6-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:bf0d47d55e313b24603bbdfcf71df5fce9b23e8a6af770024f7d7c0282dd1e60`  
		Last Modified: Thu, 27 Mar 2025 19:19:37 GMT  
		Size: 64.6 MB (64565822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:654440b1a936a382604308d045dad164d1ffff6c187d9bc9c942b866d327c8dd`  
		Last Modified: Wed, 16 Apr 2025 00:11:13 GMT  
		Size: 79.7 MB (79737858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:db16ddf95e4ae81644a5f6dc54f9cc8ff04a1c472f10bb97bae40c59caed7f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c33a9900b48fd305e05cc86a2103d6863b3e6928ff78cbc87b0e40df197e01c`

```dockerfile
```

-	Layers:
	-	`sha256:88008d862b6da883a7471ba4c7240ea78baf66d2cecdf851da23eabd4709daed`  
		Last Modified: Wed, 16 Apr 2025 00:11:10 GMT  
		Size: 5.4 MB (5432153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d94363a5c39639ecaddbf815009e3ab3c65810f536aab22d8728cc9e1747424`  
		Last Modified: Wed, 16 Apr 2025 00:11:10 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json
