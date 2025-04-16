## `amazoncorretto:21-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:2118ecab4d2db8d745dd65d59a7da4a1688433d1e787550448ae9a84eb029bdf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b1d0e54f4b29d8527ddd7ffe12a9fcb1d8f9dd226132bfab379620ccfb932c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162454151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3ae2aa5163721c62e98c9f0058c3d7e87e212ec342de4495135d0f48e4e492e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b20b05cdb644fc4aa2e384037ee36dd28219097ad71dd6b4cca12651433a37c`  
		Last Modified: Tue, 15 Apr 2025 23:56:01 GMT  
		Size: 159.0 MB (159033283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:33d985641ef82a1806c3934e910134086fb7a85e340e3fd6041298a77666041c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52e13fbce715afa826da4a77221b1d10d768e0540560461342bd20a14c67eb1b`

```dockerfile
```

-	Layers:
	-	`sha256:0a6f146b1988906bdb66c3f15420be3b3736b06c620f0dba225c2a251310f483`  
		Last Modified: Tue, 15 Apr 2025 23:55:58 GMT  
		Size: 380.8 KB (380790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12e6c9092ae5f88759a02958cc6b595ecd336647ce31f0eabcdb518a65838b9f`  
		Last Modified: Tue, 15 Apr 2025 23:55:58 GMT  
		Size: 9.4 KB (9412 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:79809ab1671c2e6bd5baec34b967265a0cc0e3403565c365693106543c7517e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160296575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3f999aa99931db37b73b1bc486cd23098e3d436d751e418acf3b37fc938d020`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da8d51fd5df84ae65c889ba157085e467091baceb0f98ef1174d5bd594f64728`  
		Last Modified: Fri, 14 Feb 2025 22:38:44 GMT  
		Size: 156.9 MB (156935151 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dd88da2849fe6e821829a9648f7e545e1c1115d6b0ae8c5d12ba38d9e7baa5fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ffe8f296e286fe9753161b0538511584b2622ba11d13db6cc3c7342ab1a8371`

```dockerfile
```

-	Layers:
	-	`sha256:d669b55363fa0a8e3b7125d93a00b05083dab0962cc141e25b1da720926cf688`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 380.2 KB (380209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5570d35c25a7be8580b6bfcc3979f499662f10cf56d314b4b528d400046f9a64`  
		Last Modified: Fri, 14 Feb 2025 22:38:40 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
