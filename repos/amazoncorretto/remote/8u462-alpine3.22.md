## `amazoncorretto:8u462-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:cde7fca3f916e8d19a4969fbd46c2452b7c01cc80c3b20aec523f1468d3d4f5a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5904f81099f44d5d4d2c0f5ea838912a3481b718cc4d0d1bc0b3a4394d5c2ffe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.1 MB (104100859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c88a829d47c8ac05c61029f11a42732770573597454fddcb813b443c8564a6d0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b1b45a8d6f3dc7cafbcae06ca1fef79354b3ff830d67b9d129dc427dfabfb6a`  
		Last Modified: Wed, 08 Oct 2025 22:59:21 GMT  
		Size: 100.3 MB (100298407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9436755f8d1e9693f9212dff23b0ad6b99d05ca844deadbdba99ed8483dbdbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.6 KB (257636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f3090b928a777433b5ea28d8232a5b6f5e09e00f0b20fceffea293f26fcb258`

```dockerfile
```

-	Layers:
	-	`sha256:7e428e44312f5f9da730077a7c5ccb45c148b6570c7fbe40cd80e2f8ad449ddd`  
		Last Modified: Thu, 09 Oct 2025 00:52:52 GMT  
		Size: 246.9 KB (246941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c256718afd133e042da84cba2bf1426ed7d23df652a11d6a6e531c6994e3de06`  
		Last Modified: Thu, 09 Oct 2025 00:52:53 GMT  
		Size: 10.7 KB (10695 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:67cddbd4ae93d85bcf62b515c41697922c3de9eee79ee4fd4fc48e716c7ada87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.2 MB (104227303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf3d61d9cac8d20231519c7a4ae8c3adafa45de3a83e7857145a5f9868d9a2e7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cda6c512225e561619e005cb03d9bd8a0fd59efa6d6f27a1cac5c733a459680`  
		Last Modified: Wed, 08 Oct 2025 21:46:39 GMT  
		Size: 100.1 MB (100089234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:73252fc8ccaa40911e98fb3af5e1287410e5d09e29af963185e22a2a3b14786b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 KB (257969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8732f2ca0235d226fc9866c27da52d76b1342588e3f2f30ec36cae6c1e8def6`

```dockerfile
```

-	Layers:
	-	`sha256:2b337d9c5321e1a12f0fba1971eb04b9ec46f07b753f114906030b522634ce39`  
		Last Modified: Thu, 09 Oct 2025 00:52:56 GMT  
		Size: 247.1 KB (247121 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d9009e91ccf05033e5de0ce9828d9c8cfb984f6a345e0f73704a04a8078a99`  
		Last Modified: Thu, 09 Oct 2025 00:52:57 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
