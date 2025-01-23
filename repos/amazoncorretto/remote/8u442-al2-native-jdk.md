## `amazoncorretto:8u442-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:04422348803e348da0ac296e152ef97cf0a82f2aa92f99945589ccc5dddec7c1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f94c1d4a4d2a1a64d001e9984676fd9ef41553052279f2d91788ea77280e8413
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.2 MB (132160056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc71e518b06bc464e0c418a6872c7b851a2d92a145e826c3d2c00204d2cad7ec`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Fri, 10 Jan 2025 20:35:28 GMT
COPY /rootfs/ / # buildkit
# Fri, 10 Jan 2025 20:35:28 GMT
CMD ["/bin/bash"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=1.8.0_442.b06-1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=1.8.0_442.b06-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:937ce5298690a9c75a91c1481f1c933f32ea7abe5993cf1e00e3d9da14f18bdf`  
		Last Modified: Fri, 10 Jan 2025 22:01:38 GMT  
		Size: 64.6 MB (64590305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d996f3fef68048283727f54076f95ab734fc01d2ef19f77445ba0d2e53072a11`  
		Last Modified: Thu, 23 Jan 2025 18:31:16 GMT  
		Size: 67.6 MB (67569751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:94cc10f2286c9a2c953c3567dfea1607285d327e247db9a76f7045c33b6e7533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6076347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73787afaafb3fd88b0258ad3d2d59f354bdd5975cbfc52da0d2ec9b2e4375507`

```dockerfile
```

-	Layers:
	-	`sha256:081997f8cbfca10814e4b7b11b85b06708af79ae1c652daf773cba302e8d599a`  
		Last Modified: Thu, 23 Jan 2025 18:31:14 GMT  
		Size: 6.1 MB (6066675 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0c1d6f76802e0953faf13f243ab868e72260750e31f137e26beca2d96743538`  
		Last Modified: Thu, 23 Jan 2025 18:31:17 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
