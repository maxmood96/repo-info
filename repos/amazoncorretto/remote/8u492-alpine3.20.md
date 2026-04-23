## `amazoncorretto:8u492-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:e21f0febb325f71650ca304a0f2f34690ea70855c061e8a57ef799acd023d227
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8cde2d8fa08c01c19fb5d691bcd2245ef9ad3593f175317d20263c0a2f5c6da5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104417165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd3b37645b4617db13b24556399f3fa02623b81cca9d3df495ad67bbd5c55e6b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:28 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:28 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:28 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:32:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8684ae2231b4d2e000274de3068e8479bc86dab7f2470309687d28dbf94b4121`  
		Last Modified: Wed, 22 Apr 2026 21:32:43 GMT  
		Size: 100.8 MB (100786844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8c406b95af50ebaa5ac81afda94651be218c84000052a5021ec6c89146fa00d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8369088640045987332a64b127981787c2b589bf497d02ea35f86f3f4c9f6abf`

```dockerfile
```

-	Layers:
	-	`sha256:cb76cbd3292d4254809999e07913700baf74fb2337965d25d622783b466febe2`  
		Last Modified: Wed, 22 Apr 2026 21:32:40 GMT  
		Size: 245.0 KB (245026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6aa205247222b7282685208696b0a5952567eff1f579767efce63a1da2cdb21e`  
		Last Modified: Wed, 22 Apr 2026 21:32:40 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b6487a02cea61f9cf4fe76f70ef146f838d4190bd44cc76b3b770d227d55ed4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104663297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97789035874c9b75e2372a8711dce21d33458ac6056a1f4cd3db53c26907a133`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:48 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:48 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:48 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:32:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:607fed9a66383a82f532de20177fabb17068f59fbcdafcaf13e38c16692a3520`  
		Last Modified: Wed, 22 Apr 2026 21:33:02 GMT  
		Size: 100.6 MB (100570978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5fbffa72f0c0fc19c1badc6b4712f6aa7cf9bc69c857e468b1a0905f9d2d02a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f143f889d3720106c052c4134337d2f244801e1a01bc0d404a1a4c391b9b8b37`

```dockerfile
```

-	Layers:
	-	`sha256:b2ad9f9c07daaf699d318e9f50361ae422de684f5fe23f37d4da251ebc362b2c`  
		Last Modified: Wed, 22 Apr 2026 21:33:00 GMT  
		Size: 245.2 KB (245158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8399fa66b599fde97aa740a31c36049462e3851467ec974e8ef15167e29cacb2`  
		Last Modified: Wed, 22 Apr 2026 21:33:00 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
