## `amazoncorretto:8-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:ed1e5bdf594a9a513669c703d39e9e5b450711f93153f1f0d47a190b5a9fac9e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4ceee4ebae8aafb5012a0eb603c23d39064d08605b2593d1c0f6c2db638f4c79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45155170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9256b654a21199d93312e44f06a74d563dedd78a5707d54cc3feeb2d7a830df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5ce481ef233fa47797a4ad16225cd022369050ae2003605fdd49d657d3da91`  
		Last Modified: Tue, 21 Oct 2025 23:26:02 GMT  
		Size: 41.7 MB (41735355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0ea71e9b94bd3e4f0f6d2c274277155b2f529693e8e72a3c0814fa1919abc3b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.9 KB (195923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed2f8bba6c5ef23546795ee884cfb89adf3632f9bd9ea272cc3f803f825ab89`

```dockerfile
```

-	Layers:
	-	`sha256:b0c3156820f947b4b68c8e16d25dfc270b1c64595f011d970ac3581f84c95a56`  
		Last Modified: Wed, 22 Oct 2025 00:55:49 GMT  
		Size: 187.2 KB (187225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1f06757829622ce7a6f2f8ec432f738d90aa9f96ee76cb8f05783b06828bc22`  
		Last Modified: Wed, 22 Oct 2025 00:55:49 GMT  
		Size: 8.7 KB (8698 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:daf92d26914e4d7d5f43ad535f9c5c8eff4b74c9f5a349007894fad07d75e2f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44792072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdd0b15b2cd263047ead312591fca907288b841264a1088f6702728d5321a6ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34109a57bb9bbc443b126f3bc251fd08d97b1dab1aa0386982baeb9500bdfbb0`  
		Last Modified: Tue, 21 Oct 2025 21:49:18 GMT  
		Size: 41.4 MB (41432771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6c3238d9f290c57354bcdb3884c133424587e906489f9b756ca091349b116321
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.1 KB (196111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b72932f6b54ebd227518e82bb9ad169d7413fccad8c19ff525d9a4c8b579b20`

```dockerfile
```

-	Layers:
	-	`sha256:0b80476c24f796344ae368737c3cce85db434972d4bacc0a785a3f64ec89652f`  
		Last Modified: Wed, 22 Oct 2025 00:55:52 GMT  
		Size: 187.3 KB (187333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38c3cbcb4e40f84468877d26d6cd9072a515a44d9d706533767a13d340be7fbe`  
		Last Modified: Wed, 22 Oct 2025 00:55:53 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json
