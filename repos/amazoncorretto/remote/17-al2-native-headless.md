## `amazoncorretto:17-al2-native-headless`

```console
$ docker pull amazoncorretto@sha256:cc33f51bbfe5515e358224ee7bf246972b3747e9c77134d5844cb1e69e0139af
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-al2-native-headless` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ed1105fadcbb5e4f1f731463ba2217508c4f741cf93b662f6dc39857f65ab483
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.5 MB (150538233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b26420d8a0ff977d44bebec79ca146167095e38ea48787168454158ca3500af`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:51:45 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:51:45 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:12 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:12 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:12:12 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2e3ea9592aad33f5f11ca8c65604905de30de68b0c38dfad7dee51b605c2a2c5`  
		Last Modified: Thu, 30 Oct 2025 03:52:34 GMT  
		Size: 62.9 MB (62934068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0031e24ff85cd62d3180b724b7638c741b64788ccdffded57010b2c4378da9`  
		Last Modified: Fri, 31 Oct 2025 00:12:52 GMT  
		Size: 87.6 MB (87604165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3cd2f96fea84e372f993f1e6151319a6f3f1a119b16883485c459bab86ff4634
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5641053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:142adbe0c579fba55fe0df9227fcd49f6443d016bf19678f0bc8b5c602f55833`

```dockerfile
```

-	Layers:
	-	`sha256:036fb80a505617e6c2cb9ebb80d781be9e356a25161aa8dd4ddb1b9b5b0b6f57`  
		Last Modified: Fri, 31 Oct 2025 03:48:56 GMT  
		Size: 5.6 MB (5631759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b0e39f53f4d1203a8e22cdb84b75aac40ef714d29457f6a6be587e270c28aae`  
		Last Modified: Fri, 31 Oct 2025 03:48:56 GMT  
		Size: 9.3 KB (9294 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-al2-native-headless` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:76b4ce6a78b63fe7245777ee0b21e804f638c16798d98b0af92f952cee6bf0c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.6 MB (144624092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61dcebd78e9bc143b03b4221c709e90e94a396dc7b027c3a74ebfe9b21850cdc`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Thu, 30 Oct 2025 23:14:47 GMT
COPY /rootfs/ / # buildkit
# Thu, 30 Oct 2025 23:14:47 GMT
CMD ["/bin/bash"]
# Fri, 31 Oct 2025 00:12:29 GMT
ARG version=17.0.17.10-1
# Fri, 31 Oct 2025 00:12:29 GMT
# ARGS: version=17.0.17.10-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-17-amazon-corretto-headless-$version.amzn2.1.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-17-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Fri, 31 Oct 2025 00:12:29 GMT
ENV LANG=C.UTF-8
# Fri, 31 Oct 2025 00:12:29 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-17-amazon-corretto
```

-	Layers:
	-	`sha256:2875a69d1768080ef2331610c2aea8f8cfff54b5df360eb9feb01240a7526ff5`  
		Last Modified: Thu, 30 Oct 2025 23:15:16 GMT  
		Size: 64.8 MB (64793458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9f6c8d5f5e274f0f351a4ec989a87e5e1120d4c4f372955bc1b6b03d67a9670`  
		Last Modified: Fri, 31 Oct 2025 00:13:02 GMT  
		Size: 79.8 MB (79830634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-al2-native-headless` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eceeb97086ee4a54e5314da7f2267b7dbd76deb829cc85a121f08b5094a71db0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5457409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f150d00a9999beb1cac5437b03feb94709f83a10b932c609ea9c9544f408ff8d`

```dockerfile
```

-	Layers:
	-	`sha256:156dc98e131f7a7e8ebcfd8f17f65e390ac87ff82a8588ca096624ac20e82ebd`  
		Last Modified: Fri, 31 Oct 2025 03:49:02 GMT  
		Size: 5.4 MB (5448035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ea7f420b0c983a9bbd45856664631849577a328228b0f2cffab44a054b76c25`  
		Last Modified: Fri, 31 Oct 2025 03:49:03 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json
