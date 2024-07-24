## `amazoncorretto:22-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:e7ca9b49fd40cc114bedd9936b4b882ecf87937878d087612c98aec331e94dfe
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7abdfc9baef81e44c6ab45fcd9d4f0aba131b1e0457ef845d04f0ee279ab6935
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161015383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41e01aa504a629f239ca10fb8474eb69e4bd10292d6d7759c8802d89a159641e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:855d35a97ed22b941f38e8185a2bef21a75dca900fecdedc9a52ee76d2405967`  
		Last Modified: Mon, 22 Jul 2024 23:06:44 GMT  
		Size: 157.6 MB (157596343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4357083d6d2fae811e419bba407af4601409e90cbbf440f76b1434d3423fc55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.1 KB (391075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e968a4a9fed2208aefc8595eabf1d9c2337738f9fcaba55a1b6af5d10b09d74e`

```dockerfile
```

-	Layers:
	-	`sha256:8e331868831b9c8bcfd84b11ef77ef011a4f50b78845dac714e7152d4986b66b`  
		Last Modified: Mon, 22 Jul 2024 23:06:42 GMT  
		Size: 381.9 KB (381906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:21c319d11312bb2960ae3e67a942cd7e2abf139e7c05978f8e720d1c8a605ac1`  
		Last Modified: Mon, 22 Jul 2024 23:06:42 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0050257c6e637f8576425a50fd6597e82b421766133f46fcb1962129924a7a5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.6 MB (158553226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:589bde3e7a210c9ba7a93e0a23b98dff1d55928a5403f9b3d2aa504f6801668d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:7990c7edbcf2739c4b2df767635f403325689f42de6e05e9d81a79fc719930c5 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:119661e64d8d593a625274dd829d8550c61de6dd5631287dfea42e99c1c2c736`  
		Last Modified: Mon, 22 Jul 2024 21:44:49 GMT  
		Size: 3.4 MB (3358458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11d245759e628c90d7e9c1130a5b397e4f13f39a4e51f0e393785fdabe787709`  
		Last Modified: Wed, 24 Jul 2024 10:48:10 GMT  
		Size: 155.2 MB (155194768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:66366342f06e385b6c662282f29377b2834af34eac5cd0e9174b25c35aeb9716
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:943ea3381299d95337c8d9bf42326d62d6b72e663ebd619fb7d71011b98d0b7a`

```dockerfile
```

-	Layers:
	-	`sha256:fa5f298568eb8e060771e5d1bbbb03673af293f8b1a84de7664e737ba5cdc712`  
		Last Modified: Wed, 24 Jul 2024 10:48:04 GMT  
		Size: 380.7 KB (380683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca25a33b8918b7790064e99add86be9f0fe625c5af480507f646933559152db8`  
		Last Modified: Wed, 24 Jul 2024 10:48:04 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
