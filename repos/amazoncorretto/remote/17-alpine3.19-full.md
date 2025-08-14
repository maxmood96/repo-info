## `amazoncorretto:17-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:c9c64948efb8887ac50724d9c614f99e267bcb48142942a038c79d7190031f3f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cb9aca8cc242669a776aae9f7fe24fc1ce32421b7829828f1de48f37916c9e50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.4 MB (149442754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56d36cd8fe15380c8e711bcfed2d10301613f2af4e26df21ae3b44be5670d944`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=17.0.16.8.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4400c1e0fc29a98d91740d97978dd9fa0b643f37332e2eae9d3607d43420d6`  
		Last Modified: Wed, 16 Jul 2025 21:50:40 GMT  
		Size: 146.0 MB (146027226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e2bb6cdb7baba6d4e7de40ab41c16db88004c80509caab6aa541b9ac1a2ee8e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.9 KB (391903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24323ce03054723e0bfe2ab486a59810c21e950e194f529f4a6425999c687682`

```dockerfile
```

-	Layers:
	-	`sha256:f00e6cb88390660588ca5c45725aa97f2fc46ca888ecb4600c4be1a5150dbd17`  
		Last Modified: Wed, 16 Jul 2025 21:48:56 GMT  
		Size: 382.5 KB (382486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfafe0394a592932666214fbc7be7cb89c15fb1ebeb79d33f6365908323a131a`  
		Last Modified: Wed, 16 Jul 2025 21:48:56 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4dd1a509dd11849784787aa0d4831671ed8f4ce70fbcd86854111f42a0f55aad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.7 MB (147673541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4988d4ed59081daf55f4431c943497e1dbed311e170288552394e81fcda29ba4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=17.0.16.8.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4e6b7b573c0ea2ba9f56543ab4986cd6a6ff0b99d837fa7ab7f68e0471280a`  
		Last Modified: Thu, 17 Jul 2025 03:54:32 GMT  
		Size: 144.3 MB (144320438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f2659bd65086409667bfa84cb0fefc2d4d3e21947f7bdc79f669a519d8c7b275
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 KB (391426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7e5e0d34d5627f1d506713a9bfbb7bd4eb7499876864a7596803b95358ac9c`

```dockerfile
```

-	Layers:
	-	`sha256:4da51612da487f32574c804dd90637be428ede982bbf04a6756adee61b64c8bc`  
		Last Modified: Thu, 17 Jul 2025 03:48:52 GMT  
		Size: 381.9 KB (381905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db334e72bc00f77683d9449d8d31af9fb56acddecd9b8f8900b7d2f238807407`  
		Last Modified: Thu, 17 Jul 2025 03:48:52 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
