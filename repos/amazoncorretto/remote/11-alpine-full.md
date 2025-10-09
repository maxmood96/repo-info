## `amazoncorretto:11-alpine-full`

```console
$ docker pull amazoncorretto@sha256:3df1c3d0d2512fcf2ac7fa5ffa235514ca97cf52fb6ec6fb66177a666658c320
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:05a49dcdc4b2504ac305ab5d1d2c106aff89d4615ea9309df4191b55b1b63182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.9 MB (145871013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f9239e213ba7ea4c41c1e30a320802c1091d77e5556fb7715eb7f95ff00a704`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5a24b29ca27afe656add599df0b8a5249fc64a0f4979f631df51be950d768e0f`  
		Last Modified: Wed, 08 Oct 2025 23:41:22 GMT  
		Size: 142.1 MB (142068561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6e8d0bdee439bf066bb3d8be8a3c99cdcb24c6821ac3eede35b32e24aaa238e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.4 KB (398384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adbe70b796b4c7ff93c7969249b29caec5d2a0d4f069c0828ef1388955ee0d3e`

```dockerfile
```

-	Layers:
	-	`sha256:2e01afa2302a7d32b4dcf12f4ed29a52da7694cebcb1b758152f00b50454b84b`  
		Last Modified: Thu, 09 Oct 2025 00:47:22 GMT  
		Size: 387.7 KB (387659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cebb11f7095d3a77253b4c93400021b989a3018683742406ad45ab63d63a74b8`  
		Last Modified: Thu, 09 Oct 2025 00:47:23 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9f62f20f3ae72f5d49397f7b47c2f4275eb6216c79816aee6098bb5d8f609b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.4 MB (144376400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4aefac675f2937093282c931f87b6088c372ce433afc8ad28a405caafd9d3706`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:99501463c927a205c2b6485b50267ae9cfa4a3323ea3012dfae186d1c1bf4136`  
		Last Modified: Wed, 08 Oct 2025 22:59:03 GMT  
		Size: 140.2 MB (140238331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f7d5b056fbd721dddf71b99c51aced492bd89ab5967888d451dceb3b13320709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.6 KB (398639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78fd8c4f253ecb4f3f8a3fa4a3611c5cc4a15424a4b9f278ab0baddd95e7abcb`

```dockerfile
```

-	Layers:
	-	`sha256:60ef7cff641b474baa630cf8ae9d52a6ca0040826fcfaa4dfbd52822fc7fea62`  
		Last Modified: Thu, 09 Oct 2025 00:47:26 GMT  
		Size: 387.8 KB (387763 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c1ba47207a17ca670f6fa771ead5d3acd1639c7475d51a4d510be5ab5984b61`  
		Last Modified: Thu, 09 Oct 2025 00:47:27 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.in-toto+json
