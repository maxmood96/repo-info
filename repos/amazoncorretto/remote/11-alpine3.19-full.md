## `amazoncorretto:11-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:e4ee0489a0c541ed2c270900b1f871327c3260423b5d6ef2d7944438f1e4f0a0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5175d01ebd00b76e736fefc3328a15f5c431258892519cc271c01194cf76e975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145330082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:167d589f83aef541ff9cd64105cdb363e7a909837831adc24c2fb6f4a857a757`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081c9810be258f47964fe6e4dbf1847ca1d4e93c2b41855fff86ea60647d6eda`  
		Last Modified: Wed, 16 Oct 2024 17:56:13 GMT  
		Size: 141.9 MB (141910376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2ac6dd940c70e69c5c1bb536abe95846fbdf2dd84dbe9836d65890014dcf466c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.4 KB (397447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0053bdf349d8e79da3e0e9456f7111b2e5f9113670e567406bd0f8ee84468861`

```dockerfile
```

-	Layers:
	-	`sha256:603685f6b43dd40186a2ee7da38ae399bd2251590aee40165933a78a8afd0a71`  
		Last Modified: Wed, 16 Oct 2024 17:56:11 GMT  
		Size: 388.2 KB (388237 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f4f47fdde40613829d30df3708aba1033cb3601fa03b19824d3fd7f6ad93969`  
		Last Modified: Wed, 16 Oct 2024 17:56:11 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0e5c83c77262a4b01f17b67dd17c2264ec174e6c7da061043c8904557c9b57be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143390373 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c09211754d96d4d737b113ecc7b71c22b163308e0d832dbf6e09aa435ce379d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=11.0.25.9.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=11.0.25.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2f175025c71fe81fa6967a804016bf4f8703d9f31e939580fab33fe0d1a20f7`  
		Last Modified: Wed, 16 Oct 2024 18:18:30 GMT  
		Size: 140.0 MB (140031270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:febff95d4a16541c909e2d2ac5b28290c0104a12688f45847b1a0b32d4d62a59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.6 KB (397601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:698088986af2e63d601b8becec68afeeac93259d37c5a45314b0e34a01ea960a`

```dockerfile
```

-	Layers:
	-	`sha256:9729b8da01f2b642a90376fcb41ded411d3f8287dc533c4ae3ddf93380d4779c`  
		Last Modified: Wed, 16 Oct 2024 18:18:27 GMT  
		Size: 388.3 KB (388293 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0aba1ffeaa092721cb069914c3e9dd694915ef48147e78ad7eb5abe51219639c`  
		Last Modified: Wed, 16 Oct 2024 18:18:26 GMT  
		Size: 9.3 KB (9308 bytes)  
		MIME: application/vnd.in-toto+json
