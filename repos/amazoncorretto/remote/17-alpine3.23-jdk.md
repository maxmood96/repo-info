## `amazoncorretto:17-alpine3.23-jdk`

```console
$ docker pull amazoncorretto@sha256:efb556c2994b79d5b4dbfbed803b552603ac9157ac3dfadaf8f8f631badf5066
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:db668792bc278c8ffa9113d92407a4640c22874e34ee6b34cd9cdf805a49dc72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152227276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5220b5ae21ae6bd0bebdac78df673c993f7b612c0373a1c380b2a915968e170f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:43 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:00:43 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:43 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:49:00 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9893ff21f339b1dac915f0c4f4babba1b9eea3f0737be3f8bc2cf8e11d24c0c`  
		Last Modified: Wed, 21 Jan 2026 19:01:01 GMT  
		Size: 148.4 MB (148367172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5d31417d8fd756372aae80e5338afc9939023cca283cfae79da929097f0ea0e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb98943b13e7f2da57dab8d2ce4b583f9fd67b6603ed17b4ec4313f5367fe12`

```dockerfile
```

-	Layers:
	-	`sha256:e9fadab753e028e61d0a11a6bbe84ac67b854a3e97c01881b63affd6e27f457b`  
		Last Modified: Wed, 21 Jan 2026 19:01:00 GMT  
		Size: 583.1 KB (583137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ca3dd43286e0cec425a92376f105a07baf7172d9f8270368cc3a9e907827dea`  
		Last Modified: Wed, 21 Jan 2026 19:50:15 GMT  
		Size: 10.7 KB (10682 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:87324e2bd77a97a01b453424339b2abb43cfaa557fca2763119de309108fe3f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150908521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:951f8c3fba566ddf57f3f66ff88b85ea139cd66bd1764cd488a945e1876d8ad2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 19:00:59 GMT
ARG version=17.0.18.8.1
# Wed, 21 Jan 2026 19:00:59 GMT
# ARGS: version=17.0.18.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 19:00:59 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 19:00:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 21 Jan 2026 19:00:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e8d87d09c2d3f260e5b0cfb420b36d5fd6729f2919f45b00056a792a16bba98`  
		Last Modified: Wed, 21 Jan 2026 19:19:15 GMT  
		Size: 146.7 MB (146712782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b4e981828dbed1fd40e278ca28a21a8e9a7740cebd4eabb86adb389e32543cd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 KB (592788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ddaf826e8a546cc921948f04c6ee2d1d149492d553a919744f833d9e9d3d63`

```dockerfile
```

-	Layers:
	-	`sha256:21ecaec9c38782a8f00cca242aa2a9a992fc82272231feb3e834f49b5dc44a22`  
		Last Modified: Wed, 21 Jan 2026 19:01:14 GMT  
		Size: 582.0 KB (581954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5a2f1735c2e22caec275e51268cf91f99b60a089135cdacda55179cb4a290c1`  
		Last Modified: Wed, 21 Jan 2026 19:50:21 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
