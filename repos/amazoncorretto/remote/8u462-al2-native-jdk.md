## `amazoncorretto:8u462-al2-native-jdk`

```console
$ docker pull amazoncorretto@sha256:7efcd58a18b0223883a57b44ce53fdea5bd17f6f3eb8b03120bb67f17e514a15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-al2-native-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3480aad4032bc94460b5484cee4e4727a690d7dd2fa28be7e7bd24bdf0fad70e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.2 MB (188200199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bb8a657a2a7f97da83746ef45fdbed2b259b3373ff93d70e37acac2725ab37d`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=1.8.0_462.b08-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:91f0f90aeef889cedc2e056e6976319ec5d96df70bf35b1d46092d2c1f375f2b`  
		Last Modified: Sat, 04 Oct 2025 04:29:16 GMT  
		Size: 62.9 MB (62940620 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:027178c47f8325ddbca4f21783e287bc6abd104ebce14271550a06e8bb732720`  
		Last Modified: Mon, 06 Oct 2025 21:10:23 GMT  
		Size: 125.3 MB (125259579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a00baa4882d157469d0b3ed7c8bda2178f43016a7d44febc3d0ce7c0221b6f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7987007 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3f412886655e1fbdfff2b06c67a145bdae5ee4e7c5793447b5ca3b1f3df6660`

```dockerfile
```

-	Layers:
	-	`sha256:61398e58db9e4ae41e5e412df08cab498bda6c865e0ad39525916ba624a22b80`  
		Last Modified: Tue, 07 Oct 2025 00:52:33 GMT  
		Size: 8.0 MB (7977414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d5c53c1433e4ee7f8da0327d3de0120873e7c5c6615d9c70524ab88234aa81b`  
		Last Modified: Tue, 07 Oct 2025 00:52:34 GMT  
		Size: 9.6 KB (9593 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-al2-native-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:791cd05dab151275693c2a1a8d5fcfa53c786932878627949588b4a2efd87e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **132.3 MB (132347108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed992d9092e16278e6a5170e81586c874e58f65b9e4a9bc8ea1381a667032a3f`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
COPY /rootfs/ / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/bash"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=1.8.0_462.b08-1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=1.8.0_462.b08-1
RUN set -eux     && export resouce_version=$(echo $version | tr '-' '.' | tr '_' '.'| tr -d "b" | awk -F. '{print $2"."$4"."$5"."$6}')     && rpm --import /etc/pki/rpm-gpg/RPM-GPG-KEY-amazon-linux-2     && echo "localpkg_gpgcheck=1" >> /etc/yum.conf     && CORRETO_TEMP=$(mktemp -d)     && pushd ${CORRETO_TEMP}     && RPM_LIST=("java-1.8.0-amazon-corretto-$version.amzn2.$(uname -m).rpm" "java-1.8.0-amazon-corretto-devel-$version.amzn2.$(uname -m).rpm")     && for rpm in ${RPM_LIST[@]}; do     curl --fail -O https://corretto.aws/downloads/resources/${resouce_version}/${rpm}     && rpm -K "${CORRETO_TEMP}/${rpm}" | grep -F "${CORRETO_TEMP}/${rpm}: rsa sha1 (md5) pgp md5 OK" || exit 1     && yum install -y $(yum deplist "${CORRETO_TEMP}/${rpm}" |grep provider | grep -v log4j-cve | tr -s ' ' |cut -d ' ' -f 3 );     done     && rpm -i --nodeps ${CORRETO_TEMP}/*.rpm     && popd     && (find /usr/lib/jvm/java-1.8.0-amazon-corretto.$(uname -m) -name "*src.zip" -delete || true)     && rm -rf ${CORRETO_TEMP}     && yum clean all     && rm -rf /var/cache/yum     && sed -i '/localpkg_gpgcheck=1/d' /etc/yum.conf # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/java-1.8.0-amazon-corretto
```

-	Layers:
	-	`sha256:8b6c0dce7361457a1cee4518c5dc9c75ff3fa343c4460bdb254d7bd18bc1bf03`  
		Last Modified: Sat, 04 Oct 2025 18:25:08 GMT  
		Size: 64.8 MB (64793208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e90e3d877e528158b668f7abd4e8af5e398e684cec7b9f909f2ca7bdfa00268`  
		Last Modified: Mon, 06 Oct 2025 21:10:34 GMT  
		Size: 67.6 MB (67553900 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-al2-native-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:09bf5bae3c590c1ac338b45612c47ccbe4d5eedaaaf8e2748984189d8eca7013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6092609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ee26880bf8dc4b17422aa712d67071384641d8f5fe4129357d8afb0a7823cd`

```dockerfile
```

-	Layers:
	-	`sha256:e10c1bec1bf4f0418847b6342ea3b80139c79eeddb879bd6bbe2773eb3068894`  
		Last Modified: Tue, 07 Oct 2025 00:52:40 GMT  
		Size: 6.1 MB (6082937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9a2cd68d7f63d27a508c0f05ba099cf49e35ca9c04d2c423fd534082caa48108`  
		Last Modified: Tue, 07 Oct 2025 00:52:41 GMT  
		Size: 9.7 KB (9672 bytes)  
		MIME: application/vnd.in-toto+json
