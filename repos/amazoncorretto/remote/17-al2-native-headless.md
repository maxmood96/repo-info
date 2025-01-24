## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:88daa6b9be2d988032e7555a3770f75953ee5a843d739079e1e1510ff7c453c2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1aee3646548640ce519cad2fec8c3b43f3e022bf2e9a482542f7b294cba970d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150030428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cb851b502d0b1b7750ea787e03e1e01d4a6c1ac8e7dd5e0c0bd1baa9c8b192f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:24 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:24 GMT
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
	-	`sha256:9fe0de22bd8b7f693a2d87aff899a83b863c2f1cc5f64f563c01e4537bcf04e8`  
		Last Modified: Fri, 10 Jan 2025 22:01:24 GMT  
		Size: 62.6 MB (62635830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69a9a9bd59e90d317a1175b9b635106f684e0d648c42d8175a0c797505a93b36`  
		Last Modified: Thu, 23 Jan 2025 18:27:29 GMT  
		Size: 87.4 MB (87394598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:528947364775ac8bc17d86465dfe94b07ce69e1dc48c38b4d17edacbd6c60210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2d650cf3787118e58ab9534c3d1ae4ed8e85986752d1d4a5eede517697d266c`

```dockerfile
```

-	Layers:
	-	`sha256:868a3e89d0e111c5197aa539f010b09a3f884dcb729ba1206b2abd6e44496645`  
		Last Modified: Thu, 23 Jan 2025 18:27:28 GMT  
		Size: 5.6 MB (5615849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d05c23f0fa499607d4fe59c2cd16ded1f54e2d33fa62a2b38b7e126fb2b3833`  
		Last Modified: Thu, 23 Jan 2025 18:27:28 GMT  
		Size: 9.3 KB (9336 bytes)  
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
