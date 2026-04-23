## `amazoncorretto:8u492-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:3fa53692c6433dbd4307dfaae1e91e21b0abd63a1303faab440b4eb205ffa683
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0e35393b64b46e049081818eacca866444c78af5fad75e68f6758e9235a52b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104595481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dce700e479622b95590a544fea88a58b096b718d93838f773e713964f2675a81`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:33:15 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:33:15 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:33:15 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:33:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:33:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07cfc17669da10c8dff97d1d088a145e6cf242c62e18be263f4f3c79c22109b6`  
		Last Modified: Wed, 22 Apr 2026 21:33:30 GMT  
		Size: 100.8 MB (100787292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:25eab1524d3b5d1bb92f76aede40e76504a34a2255634d6e506d6a50a6a73896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.0 KB (257029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f08b8b060a9c9841fa3eb030962fe84a01ad993ca453be5b11c09d71a31b0ee`

```dockerfile
```

-	Layers:
	-	`sha256:3fd6bc049fc113895cb0db6756f273c7a6fd56bb1781c1c5cdea9ae76d6a2328`  
		Last Modified: Wed, 22 Apr 2026 21:33:27 GMT  
		Size: 247.7 KB (247674 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff28543ac90cba0621fc5b567e83652ca04068c79e94f62ed1a6109fa2dbcd01`  
		Last Modified: Wed, 22 Apr 2026 21:33:27 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ef52fc69150203ed64c50fc942bfe58baf5524a95f1ed00218df3eae47e369e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104713424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de8f419dca0fb9b887a0e276e502df0a8fe7b947be0dfdf768fae0e23fab9f57`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:26 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:26 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:26 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:26 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:32:26 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd4591a6721c97995bc13c81e4c521f2af7ef968f8442cb48b2c3d7fdb4ae73f`  
		Last Modified: Wed, 22 Apr 2026 21:32:40 GMT  
		Size: 100.6 MB (100571530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3dc82e826a11c7f897776a811efc8d8900e323d8a960acc9c1c38185181e2387
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.3 KB (257265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e93dde2c52d2c7b2536218f6691346da65fb4ad86b1f863ec0b93bd0fe8df36`

```dockerfile
```

-	Layers:
	-	`sha256:e4cdd9886d2da5c6dba03414631c4655aae210f7c86aa2e04218ab8632bb7cbc`  
		Last Modified: Wed, 22 Apr 2026 21:32:38 GMT  
		Size: 247.8 KB (247806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ead07b86f103ba6c3c9d93d9d7261fa6b0aa8e93acfa5d025c44a30bfefd5664`  
		Last Modified: Wed, 22 Apr 2026 21:32:37 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
