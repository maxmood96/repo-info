## `amazoncorretto:24-alpine-full`

```console
$ docker pull amazoncorretto@sha256:8453a8659c6a97bffcc46508f4f3d4af467ca6efe542e7c540f0d704376fded7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:458e562e3591129a0a94074eeb06857fb0450ecb704208ca79ce2c62df9f26a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.6 MB (180570486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c41389ed14818e2e5d08121f202b89b5f22111967f96d36bda1297cfb854fed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6044ea9c8a1ef640a4f19ab13afda53c68d55374d877a5f49f223648ee77d0`  
		Last Modified: Fri, 18 Jul 2025 20:07:59 GMT  
		Size: 176.8 MB (176770797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cb9879cfe13d8974e80311845cbd6106f5568e74f8764fe4fee2e66aa49e649f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.8 KB (405777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69b718e1f43978408ba185bb2706a4165cb40fa9f4018f1674f25bbd1bb38d88`

```dockerfile
```

-	Layers:
	-	`sha256:81be95d87010822512d5c512225c0aa4886af6649129046c697744a13221f7da`  
		Last Modified: Fri, 18 Jul 2025 21:48:38 GMT  
		Size: 395.1 KB (395056 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfcb6046d4f90e549387c08f0db752fcd4a0f37d30d5d472c0a7bdd84ec80594`  
		Last Modified: Fri, 18 Jul 2025 21:48:38 GMT  
		Size: 10.7 KB (10721 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:57fe5855ea3c8af8581e072fadfc6591f24fa4d3d4d3b54648498a91cc3ee5ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178648147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ebe1f78929de6127a107289e0e7595a760d798ca42e6caf30b389f6ee21433`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=24.0.2.12.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7de9585f1b7564cbcb01d30dbbbf1693f75039bedbf47afb1c24cb8380f5d989`  
		Last Modified: Fri, 18 Jul 2025 22:13:41 GMT  
		Size: 174.5 MB (174517397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:74bd87db63e2bbc8dca205425bf6fe01b31802064340902349f9693958d852a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **405.4 KB (405393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c50406fdc9b56bde909701edcc7a6488ac556baabcf83533bf26dd7a8d34aece`

```dockerfile
```

-	Layers:
	-	`sha256:970fe8999c52cd63e5cb8ccadca168a1e11154e3ed984808f01d636bd846283b`  
		Last Modified: Fri, 18 Jul 2025 21:48:41 GMT  
		Size: 394.5 KB (394520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:474d96f870e8e4a24caa4c988838989399e335328f4234286bbe34166c4cbbc4`  
		Last Modified: Fri, 18 Jul 2025 21:48:42 GMT  
		Size: 10.9 KB (10873 bytes)  
		MIME: application/vnd.in-toto+json
