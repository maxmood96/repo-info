## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:3f5b762f55e3a636361b021de031f3d8a4ae10914c90a7dc64c5934516260e83
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:09b4b208242b649d7237369e9d006a3b7754b2c75fb5af963832e06289e259fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45531335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21639b76970e996e37881f71beea58f1d7b437029863de074a553b4beffbb771`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=8.462.08.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98649383782066ff15c967d73902a7efc01075197609731ff044f06083d2db85`  
		Last Modified: Fri, 18 Jul 2025 19:53:30 GMT  
		Size: 41.7 MB (41731646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a8674a07e67b73b3faf57c51c3ebf2db9bd924976ca39608cbe20188945645ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.4 KB (199393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d358d675b49932396b34dfe861d09686ce178988099c46a00dcae8239487333`

```dockerfile
```

-	Layers:
	-	`sha256:d33d56396b908f16b7b8c90634819fb64503670809000814a3bca2f029f4d00d`  
		Last Modified: Fri, 18 Jul 2025 21:49:09 GMT  
		Size: 190.0 KB (190034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:403b847e445a2209607ba4d4e3a410e38316349799a24c81cace3721c40657b6`  
		Last Modified: Fri, 18 Jul 2025 21:49:10 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:edf84202987175d0e12e869af70efec3626b854e27315fd1d92a0308053a6fb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45567808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb43e644d03c0b4580826a41ba86a1f02af9871cfa7d5078e9e56958abf83b1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=8.462.08.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:922be736b26dc4f4c8414273aa7d49c9c9043876ef714459dcf2ec83d00fd415`  
		Last Modified: Fri, 18 Jul 2025 19:53:30 GMT  
		Size: 41.4 MB (41437058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:08d7d7a2e29c9b12e7a2a5bbecb6c6b18b7f28e8a48c6ab0a804606892738787
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **199.6 KB (199629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7db400f7bc9122ccc82beba00d954a353d215aca1def228e5df24edde918c8b`

```dockerfile
```

-	Layers:
	-	`sha256:1e4fa416abfaab915b12caa0260c2c9435300286e9e4ec53dcfa9865c8dac8bf`  
		Last Modified: Fri, 18 Jul 2025 21:49:17 GMT  
		Size: 190.2 KB (190166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63f55a8c3c7c4d0c4f47176c7f5dfb3074bb1c59b193a52874544872c2874254`  
		Last Modified: Fri, 18 Jul 2025 21:49:18 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
