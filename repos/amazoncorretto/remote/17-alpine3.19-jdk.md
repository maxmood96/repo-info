## `amazoncorretto:17-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:682810182609e3148d716b05a48d886a5e82f7d4207321b045d9b564b70cc3d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0ab5d7366c4549b77963c02548d1ee19c6e8b6393c32267a2bf62785b68e0355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149446960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:407a7bea2cdab726ab39bafbebd2d0659654158ab3a6c63c39c6bd8bc688544f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7622904e809fdab80d7ea97f2f013a0493330ad1c78e050b7ee7c75ca8aca424`  
		Last Modified: Thu, 09 Oct 2025 00:57:51 GMT  
		Size: 146.0 MB (146027145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f120aa489dce6e01704cbe6e57269697978cff40e13e48a8b3bf62174cba189d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 KB (391902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a929a02fb0adb1ee7383e262286c6614dc422bae172320d94f8da60b1a6f35c6`

```dockerfile
```

-	Layers:
	-	`sha256:cb0b21afd1b44918c6312d7770867a6a554556f42cc1c58de768db2d54970cdc`  
		Last Modified: Thu, 09 Oct 2025 00:48:42 GMT  
		Size: 382.5 KB (382486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f0e0d999e742c040ba166f3dae863e01be37a2dbecf63cd1e37e6792b6d0d28`  
		Last Modified: Thu, 09 Oct 2025 00:48:43 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:902a4a68e699fef15ef512df293aee7074f819c545190ed016f643b0f327dbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147679739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3bb96db0ecda233d7d1a17c2fba39e24a9f96d4fa4549ea6c4b126078adea6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=17.0.16.8.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b5f22a1148c6a9a945ed1e27d9099e9a72c3ab847b1877665ec0ee4e307431`  
		Last Modified: Thu, 09 Oct 2025 01:53:42 GMT  
		Size: 144.3 MB (144320438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:672bd9e52053090b5be322c2c8ba658a025db076301f990037c046286cb01c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 KB (391426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5fff7e82cc132ab50cd12379f5c0e64aafc04cde2d16d400453083be3072c89`

```dockerfile
```

-	Layers:
	-	`sha256:dc14b38e9f8a7aeab29ef3aa4ef6d23de0403c1017e554ad20250af9766ccbf1`  
		Last Modified: Thu, 09 Oct 2025 00:48:46 GMT  
		Size: 381.9 KB (381905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e20e0662d99baccfd1c7d3939f794c0f51cf02b27bb8806f4cea3df32150908a`  
		Last Modified: Thu, 09 Oct 2025 00:48:47 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
