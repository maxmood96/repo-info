## `amazoncorretto:23-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:683a13cf44b44f08c1d6765af7811ad4a0304fac8cca3ea4890e57e2a44e3ba0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7560ccbc45aa0adc6fce1381af4d41e50195e779d3da058737505693eb0a6459
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170059090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad262149cf37497cf1e523ab20e90450fda39d50cc1a392f9cc8121050b3e60c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37.1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Sep 2024 23:46:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d7bb7aeaccf9e82903aa6eece2d7fae618830ddc9f136b953db7b12d3156468`  
		Last Modified: Fri, 20 Sep 2024 23:56:09 GMT  
		Size: 166.6 MB (166639384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:2312462f23ef433021936080d391d485f86b99abf68b6b7911c6390b8f441143
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **11.6 KB (11551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69e340714a8609fcb64265e53a350f4486d6a779f5cf82e604887bdd7a37bb1e`

```dockerfile
```

-	Layers:
	-	`sha256:b73f04d8c5e7bcf1f4b6ad57f485d1de81e3b91ec7bf16081cb6182da065e563`  
		Last Modified: Fri, 20 Sep 2024 23:56:04 GMT  
		Size: 2.4 KB (2381 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fddbc9136f07a8d288116909d5ab2acea2a9c8d6d166c74761dbd2bbc99d3788`  
		Last Modified: Fri, 20 Sep 2024 23:56:04 GMT  
		Size: 9.2 KB (9170 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0da3b476b93261bde27e9533afe792f05a0fd7ec268d13105c3687a5036aa185
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167669998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81f88d8cfd636841ffd5a6a4dfaf22c7e287dc239322409a0bab57ba702ccfe5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37.1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Sep 2024 23:46:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08cbddfd8b144a516f56bc0c9e898fab17c2b70bf322cac887c1c59b52f6cc96`  
		Last Modified: Sat, 21 Sep 2024 00:00:01 GMT  
		Size: 164.3 MB (164310895 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1702bc9cf9a3d9a7a1ac4eb6e453dadeed06b01d8a59f4df46cff4f369658aed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 KB (391503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91f0297cc49a54bf7a30b925168bc14c7e6cd95d01d9c8a2809d1a4c70bff0f8`

```dockerfile
```

-	Layers:
	-	`sha256:d4b743c77a7e8bcaf3b00fad7f2f7673885288ad9d10909c8025bc2ee717e9ac`  
		Last Modified: Fri, 20 Sep 2024 23:59:57 GMT  
		Size: 382.0 KB (382034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e53666a1e13a861317398ab2db032b6d99908e14b7616ab40e6c2b866b66c44c`  
		Last Modified: Fri, 20 Sep 2024 23:59:57 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
