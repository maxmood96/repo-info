## `amazoncorretto:11-alpine3.17`

```console
$ docker pull amazoncorretto@sha256:6f07b8caa6967eadc6e43b808b620bd3696d42f49b57e52ec78852491f8774aa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.17` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3cac2e250d8b69c6ab8daab819142eaabed4eae2e9467cc784ae93dd4a16503f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.2 MB (145203111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5e6293e3a6b72845c833514f6435230531ec334ea31854eeda27ed6f5a14ee3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:8bf458f5fbed9f27c897506538c02fb5810b70aba850bb883d2120985fa15bac in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a0f4cbe03b6df9e61ce02b3c41bbc05481842858bd48d9687614abe719303b47`  
		Last Modified: Fri, 06 Sep 2024 22:21:07 GMT  
		Size: 3.4 MB (3392194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffc6c6cdeae29db9ca2b0e4723681ea287d461f818b482ae703135341db7f6a`  
		Last Modified: Fri, 06 Sep 2024 23:17:14 GMT  
		Size: 141.8 MB (141810917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:920d3f534608f1647c8d985369f0edbb187d5e7afbb7bc2d92ff11753c9b540a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.1 KB (396134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d18724a8ad5159b96a100ff484dafbb199428a921e15bad28d933ccad8ebae`

```dockerfile
```

-	Layers:
	-	`sha256:0fe6d0d91e3e3bb07d31c045935e1de6897f975a64632c51cfe3bf6e64234a1e`  
		Last Modified: Fri, 06 Sep 2024 23:17:10 GMT  
		Size: 387.0 KB (386962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92b704f04fc4e5ca5217ec622b08383ffc5bc10eb524d175f9d78b516deafe2b`  
		Last Modified: Fri, 06 Sep 2024 23:17:10 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.17` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:51f0ca468241af0da2a0d15e93b9dbd216481036df41a565fa9d7c6f6379bd57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.2 MB (143232899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67f84a1aac3a280c5241ac6c2132e12ff8f5d428469ba3949a3b1e20560aeda0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=11.0.24.8.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=11.0.24.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fccfa8778150b3cb538858998fbbfb2b5633e19ee5d8239576f2b956b935a7`  
		Last Modified: Wed, 24 Jul 2024 10:40:05 GMT  
		Size: 140.0 MB (139958654 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.17` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28f63542b95a54fa422a598681ba6c87196f11fe9f142e5add539e9ac9c5e672
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1c17c48e493e67adbd4c86c5258630eaf42408af79223e043410d20d5250711`

```dockerfile
```

-	Layers:
	-	`sha256:7e5f13eca9aab6164a24cc539f9be5c126b30fa01d8b85a8c863dfe0a8b53313`  
		Last Modified: Wed, 24 Jul 2024 10:40:01 GMT  
		Size: 387.0 KB (387018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25fe9c36e8bdc945b42cc871243535b21a8533be7a9f03448da81a040e6079c9`  
		Last Modified: Wed, 24 Jul 2024 10:40:01 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
