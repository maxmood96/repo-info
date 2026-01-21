## `amazoncorretto:25-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:bd8131a90e8547a76f2e617f57a6ca49a04b97a0923596d7fc8309993518b118
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5eb992658247fd8ee3852bf9fa5f688800831e06d763d11fda9fd30dfc0036ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184361579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd15de6b13642811148c56ea32113342ac3468fa4f4bce0a8b9dbc7e9ae7c231`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:07:21 GMT
ARG version=25.0.1.9.1
# Wed, 05 Nov 2025 01:07:21 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:07:21 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:07:21 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f637881d1138581d892d9eb942c56e0ccc7758fe3bdc0f1e6cd66059fdfd8185`  
		Last Modified: Sun, 07 Dec 2025 13:55:07 GMT  
		Size: 3.6 MB (3642569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffafc9fa5ca622fe55233d5126e899c92e9073daf2549caba14b059e6aa0bcf7`  
		Last Modified: Wed, 05 Nov 2025 01:07:43 GMT  
		Size: 180.7 MB (180719010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8ef588dfdd2f70f07061d46fb9b4cd317f53bb52646218704f1fd111c7772dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.9 KB (604929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e916209b2956bee042933f556a85ba24719f7a55413f1ab7d8c36c59d18d53a3`

```dockerfile
```

-	Layers:
	-	`sha256:f8bcb43e53c272d2cf7cdb32a438abc9eb2ac2d37e75b4a4dcbcbef552ca0810`  
		Last Modified: Wed, 05 Nov 2025 01:07:39 GMT  
		Size: 595.6 KB (595558 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94cfa62397f36e438efeec265394d76c83bc32b6cc186b47db2eb3d4adcda047`  
		Last Modified: Wed, 05 Nov 2025 01:07:39 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:010c3ca2249afe862691d4be36ffcd87e3db3f0a3e77c0670876b2c01e49314e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.4 MB (182353555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecd1c6b7c5e9d56807dc06e961e2b0917ae6d44667192f9ede1e8bf90fa39689`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:06:42 GMT
ADD alpine-minirootfs-3.21.5-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:06:42 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:25 GMT
ARG version=25.0.1.9.1
# Tue, 04 Nov 2025 23:16:25 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:25 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c2fe130f4aabc917e559e7eed7d37b0e21ba13b44520101696887ca892e8c63f`  
		Last Modified: Sun, 07 Dec 2025 17:54:48 GMT  
		Size: 4.0 MB (3992353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:626e4f889f9a50d0fb9cabf53a86fa4d28540dbb436e8915cfa6460037a0854f`  
		Last Modified: Mon, 05 Jan 2026 07:17:03 GMT  
		Size: 178.4 MB (178361202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:25845653832d65585012f11bdf41185fca4c172afc94b60e94a9aacb5a567e38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **604.4 KB (604449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d624a6cdc6b9c3d6d663ced0d35f89253125bada0c72db1d77297397ac0a61`

```dockerfile
```

-	Layers:
	-	`sha256:852278f7f7301298eb2c99256314d503be2d8b9a5d230fab2bda96abfce81bfc`  
		Last Modified: Tue, 04 Nov 2025 23:16:43 GMT  
		Size: 595.0 KB (594974 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:624c27828f6d799c83da5ee78a92499f94d5096fafde6578983b46868ab11c8d`  
		Last Modified: Tue, 04 Nov 2025 23:16:42 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
