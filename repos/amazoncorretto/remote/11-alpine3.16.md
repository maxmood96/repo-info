## `amazoncorretto:11-alpine3.16`

```console
$ docker pull amazoncorretto@sha256:be9d81f2be1232657ec724aa9922f75590249e7c3ef7fad820cccac42163213c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.16` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e5e3c10099c6aecfbb9e88563f41df5aae7cbda89b65daef28161619280de2db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.7 MB (144651267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1cbdc507ae86d6d624cd68c2e4ad3156a68b7913d71c2094ee190732fa29faa`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ea6fad1b74200d75658eb8dc315e8717209abc93b93639b9f754b0fa6d9bf6`  
		Last Modified: Fri, 05 Jul 2024 19:56:16 GMT  
		Size: 141.8 MB (141843430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.16` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:622e9201be88f13dd90abd773c402aeca89d9ca1d2bf675d07f1a659e1d9eb8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 KB (390025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:056b84d2c00cf26017650b6dbcbdf49d49b14192f573ad88e680f4c618d00de7`

```dockerfile
```

-	Layers:
	-	`sha256:1e583d52bdf61fc0119837fcf60581cdabbff4dcf49465fcf3b5241d6de29016`  
		Last Modified: Fri, 05 Jul 2024 19:56:14 GMT  
		Size: 380.9 KB (380853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33542c584eb819efa038de8d95ca37ecfd8ae01cdad7c4fc4a7b920ac213bb7d`  
		Last Modified: Fri, 05 Jul 2024 19:56:13 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.16` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:abe682c0f1e837158abc01a34b6fc07d938916e591c4399638fb604b36f85ed2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **142.6 MB (142640010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c5e0c7831ff9019b0114b77e6f199c5ea887e4751175e4262e86ba6fb4bba04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f75449f7206cc020bb81cc77b8fb7ef1b300648c7713c4a30af92465a5e5268b`  
		Last Modified: Fri, 05 Jul 2024 20:08:46 GMT  
		Size: 139.9 MB (139931727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.16` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7bd4bceddd1cbfd8f013ec4bd891c46ea8d0338448b7d46e136545b6e4453f13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b651719419730d5e71a00f44d89476912ef57e4eaaff4afbf91e61550cbfaf36`

```dockerfile
```

-	Layers:
	-	`sha256:ab09203a3c455fccf7edaa2ca2bc5cfb190abea7410e0f7b087f57d5d859626b`  
		Last Modified: Fri, 05 Jul 2024 20:08:42 GMT  
		Size: 380.9 KB (380909 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:777789db14eee17766a26dd5ee81debde767275b2dc04c3800a13de5de229821`  
		Last Modified: Fri, 05 Jul 2024 20:08:42 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
