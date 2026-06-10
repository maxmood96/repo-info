## `amazoncorretto:8u492-alpine3.24-jre`

```console
$ docker pull amazoncorretto@sha256:31c36d38d0b63477023e53d338d56e60a4850f1a28d88e7fd343a2979a2225cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.24-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a73ea15f06cf03c5268932a53fdd2b4a2c267387a98a46a4aa1775adca5c658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45616852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa6d5ed01b48b9269f5453edce38783493646b24943fda34cc20c9adb705c570`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:43 GMT
ARG version=8.492.09.2
# Wed, 10 Jun 2026 20:15:43 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:43 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bbcbdf20500bb02c03b78b461d70ac08cb5f7519973602d33661a33afc132b2`  
		Last Modified: Wed, 10 Jun 2026 20:15:53 GMT  
		Size: 41.8 MB (41750097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.24-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1ed94c97174412da05e10d87207f81ac2af2a36e2e755b99b59de3488483805f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c11210b31fac238aaa117b42d6f3350d8c726f70930cf0b269b76937bb8fb3`

```dockerfile
```

-	Layers:
	-	`sha256:ae9af464b49f354c853b69b301bdeb852d90ae1b8821c38af0dbd5be5cfb5164`  
		Last Modified: Wed, 10 Jun 2026 20:15:51 GMT  
		Size: 187.9 KB (187938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a67f993d607248653403431f83e62794502775d5a6b798703ae0e3a8908c984`  
		Last Modified: Wed, 10 Jun 2026 20:15:51 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.24-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:185c3079f097158a2ebe9aa2359f1feb6fd52f6b8150de729f426fce6491ad0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45670121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd32ee2306fbf1dd132cce420402ac8b522a4451e66b08a903cbb27f442c27bb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:27 GMT
ARG version=8.492.09.2
# Wed, 10 Jun 2026 20:15:27 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:27 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:27 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7069ccd0f302809faf4bcefe6dd08a4083fa0db96ecb4a135afbbf9885d1d840`  
		Last Modified: Wed, 10 Jun 2026 20:15:37 GMT  
		Size: 41.5 MB (41467791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.24-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6ad19f9a5a7980d341eb67b0d728f15a89a2de302a7ce93e7557ac6530cd4e1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9836c7e779f4e5ef734ad8732fff00333d838940fa234c0346bf6291cb15017d`

```dockerfile
```

-	Layers:
	-	`sha256:863ad075c571e43e80d702f7a4ebace5de328e03409da49926d92f98f07a5787`  
		Last Modified: Wed, 10 Jun 2026 20:15:36 GMT  
		Size: 187.4 KB (187420 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7db755f2912ce9ac61f8fa4b790cd98e6eeb7f2f03281f3d243eb8cbe1150828`  
		Last Modified: Wed, 10 Jun 2026 20:15:36 GMT  
		Size: 9.4 KB (9419 bytes)  
		MIME: application/vnd.in-toto+json
