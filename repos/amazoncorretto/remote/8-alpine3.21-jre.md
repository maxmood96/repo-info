## `amazoncorretto:8-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:713fc1118af51cc80a7ea10caf2347190e1bc8ceb4f367ab322ac97a5c867272
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:777306196e4b2d3de742820aa6843801e59cb1055fee981a6faca81278a1c98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45305372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d421e287596f8e751fa9679a7de242b162a85c887f60676e53a6a50f0b5299`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2e850e8dd0e029145e8ab926ac957c6f15892e57c88266dd819421d7a350f2d`  
		Last Modified: Thu, 08 May 2025 18:36:03 GMT  
		Size: 41.7 MB (41663125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6627a177305e5f8b164cb6b5ee8bb1b28657968bf1828be7402f254347a77c1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee1b05bfa02f7d7b4ae4f8070cee4b84ac6b5a854ca46474da7770863b238128`

```dockerfile
```

-	Layers:
	-	`sha256:084208e1c231d9c7f1681bb27bd2e81ee23005e656953a30e3416a93747f3538`  
		Last Modified: Tue, 15 Apr 2025 23:55:27 GMT  
		Size: 187.5 KB (187487 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1311992688de2d8501a2f4eb28941bf5d9044594fbbdf8f0a40cc487d0c99c0d`  
		Last Modified: Tue, 15 Apr 2025 23:55:27 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:54109b12a4a59b00410fd9a7ac5531be638cfea18f493bf394e0d4faf67ad55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45358843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0437f4ec5d9ca33c616e6a48607bf453d8a630b62a62af8e4c7c516d39a61cf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5b6e8d787d1b0cf14401ed4e19785d08cd34343b2a051e2604fc77118221d12`  
		Last Modified: Fri, 09 May 2025 00:05:29 GMT  
		Size: 41.4 MB (41365814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ba53151f7071af969bc3c80b4c8a53d67f8d941ed9ee54bfe517b57bbb586c00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db7b314841a7fefbdc4068bc2686a94c0c7dec3f552cceb60ff2e5edf84add1`

```dockerfile
```

-	Layers:
	-	`sha256:755e55cac742f06f429fd02525f1ef269cfaae9d6dfe8cef5b663a0fd8654251`  
		Last Modified: Wed, 16 Apr 2025 00:00:30 GMT  
		Size: 187.6 KB (187619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ecd5c940615a410322d79fd2f851768279893b26acd76466d2f2ecd91b022cb2`  
		Last Modified: Wed, 16 Apr 2025 00:00:30 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
