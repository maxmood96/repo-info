## `amazoncorretto:11-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:579f86b04cddac9ca3afdca725e004bd5e93dce50e27e7d0747f66545e5d135c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4b924133e63b92ccea06f0f15d8905722921c8f64508aa3a4125a47e0be13f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **217.5 MB (217548208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f483ceaef1acc41bd4d89efe4ee925850bbf1f651a87add6bf3abba465bb0056`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY /rootfs/ / # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:78d6b943ec35657899afc44f3f9b766ee923d9028028da721b7d4e7bc35e184f`  
		Last Modified: Tue, 23 Jul 2024 13:50:25 GMT  
		Size: 62.7 MB (62679166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989637037a05e28458bcf670d11bd08dc8e9dfa7d8a6b16b877d4cea67e806ee`  
		Last Modified: Thu, 25 Jul 2024 21:02:30 GMT  
		Size: 154.9 MB (154869042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b52bc7e61515e160ea7e8ab8e8cdebfa2a9c0214a50df785da51d2432dddf191
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5688039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70f93016151a9759bd60107c589439772e0888ed7a3b9e4ec4c2566f1b8617c2`

```dockerfile
```

-	Layers:
	-	`sha256:aa6b93ec08615f1bdb5627c748afcd1a75660f5a182af0f4a592f1327cda0e98`  
		Last Modified: Thu, 25 Jul 2024 21:02:29 GMT  
		Size: 5.7 MB (5678742 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a624243b5fb7875f5d404481f550327bf751947a6859f14cbd8ad9eea3c028b9`  
		Last Modified: Thu, 25 Jul 2024 21:02:29 GMT  
		Size: 9.3 KB (9297 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9f68e8c8ebc35c2f41a331b3752e97161c5af29f65192a5a6e20ffca9c04cb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **211.8 MB (211773975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2463c6d56531e46eb8552db9a8eac46f6f91ec111d99201c826a7f34b864fadd`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
COPY dir:cdeeb89e10fdbe3f38b9e5f6d359ee1afb9caaa1018fdd71fd6c0374dc592a5f in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/bash"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8-1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:4ba2ef523fa6e28aa5a068ecb9167a3b9efa29481c3ecc6d34fab1c350b98b6d`  
		Last Modified: Thu, 18 Jul 2024 21:40:02 GMT  
		Size: 64.6 MB (64575311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cc7c70cc1c6aefcc09eee14f05c61d51efd453fcfc19b4aa928a750fea04fbd`  
		Last Modified: Thu, 18 Jul 2024 22:53:18 GMT  
		Size: 147.2 MB (147198664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aaf34279255dfadafa3dbef10bd94dd8db4b6b8ac5768dcb5f787ea8b5893b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5506283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c75204e9627b2207273d37e732719ea8ac1b7b9d566cc22a02789c6ee649f67`

```dockerfile
```

-	Layers:
	-	`sha256:3066fa2a151e30999a0336453cea2362ba544393ec77612c80259536438d64c3`  
		Last Modified: Thu, 18 Jul 2024 22:53:15 GMT  
		Size: 5.5 MB (5496913 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e6af15c7cc66d277ae43f1dea774c004cc3f2174535ad2820ca8a02c8bf4db8`  
		Last Modified: Thu, 18 Jul 2024 22:53:14 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.in-toto+json
