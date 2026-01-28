## `amazoncorretto:8-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:7314468a7bacd9ffc4b63a76b934129584c81ff7e6c800208c09fb3c008842f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6e6d48c99af777f63b38544d4a9e81579cefa23787e69064cbc92152b68cfbc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45548755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b10085b19b6a85d7bd71b24cacb5956e744542972a5f28636a05bf5d64425c94`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:40 GMT
ADD alpine-minirootfs-3.22.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:40 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:42:45 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:42:45 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:42:45 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:42:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d49a2dee86fb12766dd648402d010ca105846a41bd58738454e53780d4bb8e97`  
		Last Modified: Wed, 28 Jan 2026 01:18:46 GMT  
		Size: 3.8 MB (3804875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4383c58d345813c60f4ad6279df8eea400bc064d924c6689891e9be91fa853`  
		Last Modified: Wed, 28 Jan 2026 02:42:55 GMT  
		Size: 41.7 MB (41743880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:62e5b7b5107283cc07ddf5cc4464f32a733254aeb727a4434e78c1a9282133a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e7248f814db4adb2ea0e14a9b2ab5d7dce58eea430d9b92f13cf6404e7cf802`

```dockerfile
```

-	Layers:
	-	`sha256:68beee2432678265c83ca5c96eb68d325a10583c7fe14ddd09dc25c13e6865a2`  
		Last Modified: Wed, 28 Jan 2026 02:42:54 GMT  
		Size: 188.5 KB (188490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4e0112d386124264a618bc1da16c9ce7764cb6df4d377a10279e9f919db8b51a`  
		Last Modified: Wed, 28 Jan 2026 02:42:54 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d63ab47bb0a857c3aad2e4689c1b6910aa60b28374e802fe0b51f4f32b5f9993
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45596250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825dad3aee85fc5d1399aeb2284d57adbe00cd7388bc6f29d836bb38b5dfe965`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:58:36 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:58:36 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:58:36 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:58:36 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ccc627f49a1826bb4139cd35304d733c7fc6625f1175cdb145e2f7e30e1595e`  
		Last Modified: Wed, 21 Jan 2026 18:58:47 GMT  
		Size: 41.5 MB (41458181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:491e1ab953b14d58cc7794001d82f5fcba23affd4b7d81b815452a985de7d782
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197334 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693df936bf23004d3df5c19971bfeae37a481f442aada8f57837230ce83e79f4`

```dockerfile
```

-	Layers:
	-	`sha256:cbf1ce4445978621799c3bcc20e94d645c0cd247d31c38ec4d070f085fdacb9b`  
		Last Modified: Wed, 21 Jan 2026 18:58:45 GMT  
		Size: 188.6 KB (188598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99292e4907c58ef27bfbbfefeaa673f2dc9e2ae65855c1f58cc79040422fa6a`  
		Last Modified: Wed, 21 Jan 2026 18:58:45 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
