## `amazoncorretto:21-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:2a984f63f7190eeaaffb43cfa2c9a9ac5c4050506035514fc73b6c1b210954d1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:61eafdeb119539fbbeb328da83f4f196c00a9db13dc3789fffd4551caa3eb678
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162375678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91349b575f945cbbc6e7394bf395a68cb778e96b1c5b8f45851616270f746900`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
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
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208c50e5bba44ff5c675a74e24d23c7a8e0c919f9026146fac2290e43ff53f5b`  
		Last Modified: Thu, 23 Jan 2025 18:27:22 GMT  
		Size: 159.0 MB (158955436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0412382e75a162d757536b909d350dfb3763cc94501c2b12bf60f9ff701cf58d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb616a5223b0a3b55c0672499ff23c48aab4b5f3a054ca4cbe1fd747378b9b5f`

```dockerfile
```

-	Layers:
	-	`sha256:8a9b1f44111727fa96055a90e890eab109bf8339dab27cafa2fb4eea2af294a7`  
		Last Modified: Thu, 23 Jan 2025 18:27:20 GMT  
		Size: 380.8 KB (380790 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a29c500eec31909f54ab5806d56e5fecfdc71165a6d5a2932b47423c44bd20e`  
		Last Modified: Thu, 23 Jan 2025 18:27:20 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:21-alpine3.19-jdk` - unknown; unknown

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
