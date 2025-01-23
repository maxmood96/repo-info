## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:8fca2d8bec12a6bcf6256be97c4048240b1403c7c2c5e9a5c026f8f6abe8e98d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cc0d1adfb13947cb0342bc5e80df2077f48ef8d81ab8d8423baf8cfc43cc87ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150029384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e51770b3d89a6b7545c668f92d19e53e5b97bb87a431dcf040281fb3c23d204`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
COPY /rootfs/ / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/bash"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11-1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:651b94c781ff437453f3431f2005165974289f4145afaa6b8e94b2ffe11ca78d`  
		Last Modified: Sat, 11 Jan 2025 02:29:42 GMT  
		Size: 87.4 MB (87393554 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:de0f11fbf7f7a79e0768dfa86ca9abf4ac97ff57989a02a6307832d493d81b33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6e24a957da101bc3288faba5c224fe23039efe95c907885feefffcc3e4d9e5`

```dockerfile
```

-	Layers:
	-	`sha256:a83c0e995c9e5e41b3fefe7d658fcaf9c9d71e2f09e3293c9e8029f8df717764`  
		Last Modified: Sat, 11 Jan 2025 02:29:41 GMT  
		Size: 5.6 MB (5615853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c8d5fc461c1eceea2aca1d32147553753080557fd751082fae3a10af575b919`  
		Last Modified: Sat, 11 Jan 2025 02:29:41 GMT  
		Size: 9.3 KB (9337 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2adcc5181b2afa1c48bc8523c7b35e8e724ed82560c89a332a2a13dcc9f2e814
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.3 MB (144298943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b26e890d76fd128a33b5fce7aa2ce394aad44b98360e979d2e77b04c8eb0d4f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
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
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6747838aa98ca18e9ba311b05ef6392ee22cf93689b076a79861dc27e81577af`  
		Last Modified: Thu, 23 Jan 2025 18:45:11 GMT  
		Size: 79.7 MB (79708638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a7339292ec629d9ac88ebc7ce6429ee1ad48fc80dc20209860c906fbc3de26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e96283e8ebb280845e4e1be14391e54432541bbc3d14349b7129199d7523b7f`

```dockerfile
```

-	Layers:
	-	`sha256:20011acde5384758291488f1ea80faae6d5b1ea0baf7b98d528257c0806a5054`  
		Last Modified: Thu, 23 Jan 2025 18:45:09 GMT  
		Size: 5.4 MB (5432125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:627796f939dedc4a26d1e77ba6aacbda4b86b1ff54d3d0d11bdd3c29975d73f0`  
		Last Modified: Thu, 23 Jan 2025 18:45:09 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json
