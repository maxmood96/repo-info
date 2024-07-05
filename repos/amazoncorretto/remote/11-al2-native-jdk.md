## `amazoncorretto:11-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:6727eb9d68d2fcc5c5347e202dddbd1d700dd0b31a071b8c4e03e42825e9c5ba
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:59b89fe5582dc14aeb10d372f826ca18b48032f24f56001e22b8bdbf429c08f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.7 MB (224724077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c53979949387ad1ecdeeafc7e1d39be6e826988f1b7ad321fd40e6f1e2853d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:db8dc48874881c2542c8e2120173f53413158e7da7526edf07aa742f426b8c16 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2a5dc0ac7266321476902a4277a4723285b608c065fcb80cacdb3ed43a7c29fe`  
		Last Modified: Fri, 28 Jun 2024 00:20:37 GMT  
		Size: 62.6 MB (62646638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d50d708a081dd0fe3b1a18220e86b78b8f5056d488906be2796129d2eec22d`  
		Last Modified: Fri, 05 Jul 2024 19:56:55 GMT  
		Size: 162.1 MB (162077439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da47519ad0e387db626386027e96430aa856892943b6dd3244dfe31eeeeb626b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.0 MB (5974005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef6e9b9efbdada6425b7082fdb076dff531ace43777e89cd3665f53769639fe`

```dockerfile
```

-	Layers:
	-	`sha256:557aa50cc2df084a3338cbdea2943ffc27bc952746eada364fe737b8e0fab3ca`  
		Last Modified: Fri, 05 Jul 2024 19:56:51 GMT  
		Size: 6.0 MB (5964804 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0093f09e049ce4d04b46df3d6fb9d36be2de021529c5d913957e2921b30531a2`  
		Last Modified: Fri, 05 Jul 2024 19:56:50 GMT  
		Size: 9.2 KB (9201 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fa6070164d4bcb4d558f6eed219b079f8562d66ac35bed4648cb42d88d8cbbe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **216.8 MB (216819137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:982f896d7b25c9ab5d7a8ec42cba54491eab279c769f5879506bafc2d48bbe25`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
COPY dir:36542351efcfebe46f7ccbf0def8f62c4d1fc618b41a02b6d9df97e06c5cf74a in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/bash"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9-1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-11-amazon-corretto-headless-$version.amzn2.$(uname -m).rpm" "java-11-amazon-corretto-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -vE "log4j-cve|corretto" | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-11-amazon-corretto.$(uname -m) -name src.zip -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-11-amazon-corretto
```

-	Layers:
	-	`sha256:2936210a619ec662b53521cc3dd41798a491971a48e14f14ebb594e81dc798b0`  
		Last Modified: Fri, 28 Jun 2024 00:40:34 GMT  
		Size: 64.6 MB (64568765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24fc08d9d50c09b5a7e76fd06b25cffdce40c47e6ccd98027340fea577c79f6e`  
		Last Modified: Fri, 05 Jul 2024 20:08:08 GMT  
		Size: 152.3 MB (152250372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d7460a80ffc884cc2893a9fed75dd7a29d1aad2e474c8c0835b6bb4c3c3e554c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5766656 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d157d610717c101a68e54b59e411e1ca5f60c174fe2c97c9c9cab982d76aa790`

```dockerfile
```

-	Layers:
	-	`sha256:0cf3e065d04926e5c95629baf366f5c537e8d772131027976879071101b40f05`  
		Last Modified: Fri, 05 Jul 2024 20:08:03 GMT  
		Size: 5.8 MB (5757178 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a90086024889d460fd6644464de2070b2d1fb33317b10f7e52355f168102dd67`  
		Last Modified: Fri, 05 Jul 2024 20:08:02 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
