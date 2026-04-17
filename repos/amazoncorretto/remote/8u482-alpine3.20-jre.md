## `amazoncorretto:8u482-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:e84c1f50f448cd78e49f334403e665133d2e7e20cb53558fa88a4c6da5cf3419
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:47dabf07099a688c4f55d4252fc433c9f5c7768ff20018030912f35d1b2dfe87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45373235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c71dc283409f1c3c987ebe67ddacaf2aadf6064605c4331d4df5c4b01a6922b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:05 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:22:05 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:05 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d034f5b6b29da41bef276f1ab1085592590e9fdc48ce8b3d285a97186250e167`  
		Last Modified: Fri, 17 Apr 2026 00:22:15 GMT  
		Size: 41.7 MB (41742914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:38f86877c73e5cc00f2c3024765c83357784d3631b65cd4bf586341a809f7d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dd8599d2fe2d5e5b6326cccdb7004cc70125cb56a34319c9654f25f184833fc`

```dockerfile
```

-	Layers:
	-	`sha256:d41e560ab5bfe479afd927b7f46f50ae978b890cc9bc1ed9e710e3b200679349`  
		Last Modified: Fri, 17 Apr 2026 00:22:14 GMT  
		Size: 182.8 KB (182818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:514c281962da1afadd8e2abc64d8a0ac5cdbd9c6371dcbd7315791ea317eba07`  
		Last Modified: Fri, 17 Apr 2026 00:22:14 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:dc419c908e067ce084279aec5e905289d4ffa64eb0597770fc47849431900642
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45550475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cbbec3c50221f3727b1182c459496ca71521d8f894409ccbcc3351e97200310`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:23:58 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:23:58 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:23:58 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:23:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9009294bfc0223eff1c258acd4e4da292b893606e12661f7346dfa3bdbb4ab28`  
		Last Modified: Fri, 17 Apr 2026 00:24:09 GMT  
		Size: 41.5 MB (41458156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:60ec4f4a1b51cb6fd80b69dbede1b2330e96e527d23eab6f51da024359738dff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 KB (191662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b74950cbe00196f63d4e98b39fadb0f730ba42ac9c0312bf73743c4ed2a35421`

```dockerfile
```

-	Layers:
	-	`sha256:f876c8602be396e0979bbe759cb9d2ecd52689674ebf30c379972f304ae4a976`  
		Last Modified: Fri, 17 Apr 2026 00:24:07 GMT  
		Size: 182.9 KB (182926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4856aaaba6d0dc6f962850b92916ff18df714e3279f15e548115b26996fce108`  
		Last Modified: Fri, 17 Apr 2026 00:24:07 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
