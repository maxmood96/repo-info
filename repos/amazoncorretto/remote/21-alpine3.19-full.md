## `amazoncorretto:21-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:311e982d68289b1b6799647d82f2b0e22ed1b1ce5006abc416dccc2e25f6a2cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3e1a908895811004aeb5d05dc51066b891e26d6da9263b56cc31ed84d591bb4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.3 MB (162349775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0ea39f0b8f4c3d4ff4cf87d841b7c7f2d91c5044c0dbae5a2832a01085ca0b0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=21.0.5.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=21.0.5.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a687de8a81ed6abcfc4f4e46291d3e9e7af55d3a4151f62017fdb8306ad7fa54`  
		Last Modified: Wed, 08 Jan 2025 18:13:31 GMT  
		Size: 158.9 MB (158929533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e759eafc98e241680c06249c4840e7eefd8752fcddd6dce674ba7677e4be4b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99918b3dc5d630cb74caba0d77317b7b6e34c30d3f7cb3aec6043c101bc7ad78`

```dockerfile
```

-	Layers:
	-	`sha256:b3beca115967b26d8d4c087ce7ae37e6ed3e2ccc236a503acac29a4cc1df69f4`  
		Last Modified: Wed, 08 Jan 2025 18:13:28 GMT  
		Size: 380.8 KB (380792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29be517c3c3f05710eaa9dc9ad26a57de5c582572b4373e7bc483c8876e5eb80`  
		Last Modified: Wed, 08 Jan 2025 18:13:28 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1c2929845a7dedc375c55424795d02c9b9153c92ab89a80944f8543531fc08a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160295817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60a235c26aebdf6df29f1fc801880eb4e84e918a3970f52aee442949b09c4e79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8068bc7985e5bb1345a87ec8c8c043730dc5f78f17b1fa62bb67b5ae19e31911`  
		Last Modified: Thu, 23 Jan 2025 18:53:40 GMT  
		Size: 156.9 MB (156935285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e55ee5face74406c765dffd41a90e8a7051213b14debe9df67706663a7b5fba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82219d064d6394a1de9a843cb7dcdacadf44ad61ee8f1c8c5e9f2f9dbe6ab383`

```dockerfile
```

-	Layers:
	-	`sha256:7c70a50b8ab47ac3f189377754b4b89b17b81596e1974d56e29cc4255f95e23c`  
		Last Modified: Thu, 23 Jan 2025 18:53:32 GMT  
		Size: 380.2 KB (380209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97c3e4794b0abd632644b815a0cf629c1d9e541fcc0ba447c8c16db5fc30ffca`  
		Last Modified: Thu, 23 Jan 2025 18:53:32 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
