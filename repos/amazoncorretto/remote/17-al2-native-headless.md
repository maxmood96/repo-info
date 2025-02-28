## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:19c8d9d544fac0aa353e55b7d4cd4c50e5fe10b54e39df700bceef487319357c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2153282dd7a0f10c5b346d5e06b2d70c64a7108e648a61f08942ab4e808c4adc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.3 MB (150280779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e0759ac3fc46a93f386d98ba866e6a991ddd8d0b6706b2cfa225d73b5c85ace`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:7f0a890370e7b6290884eb8b70dcfcd6749f097764b13db947cdd9196f5b6ecd`  
		Last Modified: Wed, 26 Feb 2025 15:57:24 GMT  
		Size: 62.8 MB (62802042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:034c87da3ca6165d67f058b534ebdf6804d12979490664b5919947373a75a1fb`  
		Last Modified: Thu, 27 Feb 2025 21:08:21 GMT  
		Size: 87.5 MB (87478737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6438a7f48f8e3a8b461e8d238cf7b36f9d685c76ee3752ec26fe5538b81dd0bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5625189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2a358b90dd0ee89db1a1db3fc958515b4cfd6adb2417e674238a199a6e3add`

```dockerfile
```

-	Layers:
	-	`sha256:9798127efdc7f7a37a34b38b46546b8f9c776a8c8533c8a464992014ec36b00b`  
		Last Modified: Thu, 27 Feb 2025 21:08:19 GMT  
		Size: 5.6 MB (5615853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:991489cfaca6de38a0f1f84cd52e27ac46a25dccd05050e3f0332f52ab8892d2`  
		Last Modified: Thu, 27 Feb 2025 21:08:19 GMT  
		Size: 9.3 KB (9336 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:688c828c79805218ee50d36847bb7be852763423c9f31b07ec5562b28ee3b628
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.2 MB (144183200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ea4b9fb7dd27d2c34fc6badb4c318bddc062aab42b3fbec56187c900c5bdc59`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
COPY /rootfs/ / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/bash"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7-1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:5270c35d4d9446d8a0ab2f41ab0020c11889bd8617236093cc9c87563d120b9e`  
		Last Modified: Wed, 26 Feb 2025 15:57:39 GMT  
		Size: 64.5 MB (64521208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5d7b08e26ac3bdbf048e1aa48830967a3721ef550dfd6ab85bb25acd97439d0`  
		Last Modified: Thu, 27 Feb 2025 21:18:53 GMT  
		Size: 79.7 MB (79661992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:47cabaf437e2281f723e014778fad92a598b818ba540d37fccab75e144f2b909
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5441545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6494c1cae57306475c0ed71e1cae14abca1cd18c923792b63043e1557ac5737`

```dockerfile
```

-	Layers:
	-	`sha256:074bcf75193f76b781eef4d52516f128770fe4973b7b83b6fce606261cbae542`  
		Last Modified: Thu, 27 Feb 2025 21:18:51 GMT  
		Size: 5.4 MB (5432129 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9964bbcd96720fbefefee78875aaea4014c2cdda1ad2e2abc43c09144389530c`  
		Last Modified: Thu, 27 Feb 2025 21:18:50 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json
