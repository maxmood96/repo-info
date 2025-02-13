## `amazoncorretto:11-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:d792838494585740272709d329bb3d6371b0efe25b1a0bf371acb1f9cdbcddce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6d84c73012881005d904ad54ed7ed4c18e09b0af009a3b52e66dbaf4dce8931d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145329089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13cbb6b7c47f610ae3af6769682ddc0a505912b68cf0636ca35abaa44a5b39d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b05d0c9e34722b0a89573de9ce0872d7fbe166a677c439d36c5287f5bc661e8`  
		Last Modified: Tue, 04 Feb 2025 10:01:54 GMT  
		Size: 141.9 MB (141911115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b37940c4b7ca1cdfa442e9ebd9aff092001137cc50e61d045e43ea9f45ffc3e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e068801036c755fcb65b98e8290a23817e3090a849fa37d02b245c6e025e0e1`

```dockerfile
```

-	Layers:
	-	`sha256:908ad2cf9a2512dbc2230e5e8473d7431a0238c54ee8c4372f4dd8c1e08bbd89`  
		Last Modified: Thu, 23 Jan 2025 18:27:19 GMT  
		Size: 387.0 KB (387034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b81e58065b0ec44fc12872ae56901c582ef6f54d938597171de6df69ffa210fa`  
		Last Modified: Thu, 23 Jan 2025 18:27:18 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f1be038b4639151979701aeb8c0be9d9fe879b27361994ec8a6ee5df8d3e77a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143377156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffbaf16f9591a111294155156275526ad5631bf0f671ee013c1a8efb59f88b18`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=11.0.26.4.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edde409798e9c9b1f50ce8e5bd8f559d95a464f17f0cdd831122e872bb652852`  
		Last Modified: Fri, 07 Feb 2025 16:39:14 GMT  
		Size: 140.0 MB (140035295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f22a01756ba53fe4e161b3a2753483b2ed18758cbf0123a38611a4b74e227f44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.6 KB (396611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6c3df39546498dbe83adbcd1e176a565be5d3895591d0abde16efed18d7fecb`

```dockerfile
```

-	Layers:
	-	`sha256:2fe86b181d9c2236408b85d99c8d3368d8b566ee50944d4ead4da410c708ebd0`  
		Last Modified: Thu, 23 Jan 2025 18:39:48 GMT  
		Size: 387.1 KB (387090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba2ae2dd0d51a4561972fb0337c8e870eaf7a6aed4c8243a5271cd28475996d7`  
		Last Modified: Thu, 23 Jan 2025 18:39:48 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
