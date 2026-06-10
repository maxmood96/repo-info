## `amazoncorretto:17-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:43e9392d72d62d9cdbd04bc54530c33ba354a4637ab306c7300e5fc35046458d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e862119cb278ec906e9fae95ee04fb89900a5ccecb9012acf925b75981b956ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **228.9 MB (228914811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90a2929ed5913729dee828bdb19b3985f554be657ceaad4890c6d35f1470592c`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:26 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:26 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:22 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:12:22 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 09 Jun 2026 21:12:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:1b617831d6b1041202bed08e227be201a09f5bbe282304143d3ba1e6b9b6cd1e`  
		Last Modified: Wed, 27 May 2026 11:49:15 GMT  
		Size: 62.9 MB (62941950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dc03d04777b5078d67954c2574431af86461333a7130ee11a9c2d5bca8fd4d8`  
		Last Modified: Tue, 09 Jun 2026 21:12:46 GMT  
		Size: 166.0 MB (165972861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:476cf9719af3c4aa2210dec56c48a5d0f508d60ed5a240afb3b848ade897930c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5982799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd3ec606136c49bf5c383bf2c50b7ee0476b0122bd1bd4671dc7cd2160806d9`

```dockerfile
```

-	Layers:
	-	`sha256:84506c221bdd98d09fe3d27440621fdff9a356826a3eaac284fd114a921b1c0c`  
		Last Modified: Tue, 09 Jun 2026 21:12:42 GMT  
		Size: 6.0 MB (5972740 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a108980fefaf38d9e0f7a7baab90ebec480660b668852bcb12101d781b4d71c0`  
		Last Modified: Tue, 09 Jun 2026 21:12:42 GMT  
		Size: 10.1 KB (10059 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6a1fe72a5327e73970169d1d6091263bb47122ab867734d8aee71926e51777ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **221.3 MB (221263853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a056bb1e0875396b9ebc775544f392170df8e44cd6736f2db62ff97fdcca12`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 09 Jun 2026 20:16:22 GMT
COPY /rootfs/ / # buildkit
# Tue, 09 Jun 2026 20:16:22 GMT
CMD ["/bin/bash"]
# Tue, 09 Jun 2026 21:12:14 GMT
ARG version=17.0.19.10-1
# Tue, 09 Jun 2026 21:12:14 GMT
# ARGS: version=17.0.19.10-1
RUN set -eux     && ARCH="$(rpm --query --queryformat='%{ARCH}' rpm)"     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-devel-$version.amzn2.1.${ARCH}.rpm" "java-17-amazon-corretto-jmods-$version.amzn2.1.${ARCH}.rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && if [[ ${rpm} != *jmods* ]]; then       yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );       fi;       done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.${ARCH} -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 09 Jun 2026 21:12:14 GMT
ENV LANG=C.UTF-8
# Tue, 09 Jun 2026 21:12:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:592be6a6d0447cc7e4d0cd5d164508693821dd45a5dbe90f47689441f936d50c`  
		Last Modified: Thu, 28 May 2026 09:28:16 GMT  
		Size: 64.8 MB (64790709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:063ec480b7163f55489a1f588eaf4f7537a6c4162eb69ec9bcf74417c209f940`  
		Last Modified: Tue, 09 Jun 2026 21:12:36 GMT  
		Size: 156.5 MB (156473144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f4578a102b049cde6af8caab871f568eb26f0344ac5fbbbe5936c9cabf4aba01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5774751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e33fb00875e7562517219ea27c07f56e1303ec9713ca4ae7e6f055cfa2bc117`

```dockerfile
```

-	Layers:
	-	`sha256:f60b3ac20ed86942bcf7a67f13e110837167b9193a607341e052010e4fc54b86`  
		Last Modified: Tue, 09 Jun 2026 21:12:33 GMT  
		Size: 5.8 MB (5764611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a861e3ec462b11acac7d45628a0240925320299435674d72d3c2025f9fa6a40d`  
		Last Modified: Tue, 09 Jun 2026 21:12:33 GMT  
		Size: 10.1 KB (10140 bytes)  
		MIME: application/vnd.in-toto+json
