## `amazoncorretto:21-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:fda60fd7965970ce7ed7ce789b18418647b56ac6112fc17df006337bdc6355c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8003eeae6db70e3881a552c3e857f28c84cde59d9992abc2a926f3e1e40d5f33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163183733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7422787e7b99b3ad1466e5edb4a6b257fd5b4c4177a8ae114e861887acd0ceb7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b083f149c2d267ca3303423ef9bf313bd8ed46afb1e9070b278f0f1cc4924e65`  
		Last Modified: Fri, 18 Jul 2025 20:07:40 GMT  
		Size: 159.4 MB (159384044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c050bfe81dd7d854e474121160041d19eda78bf6d13d1fc6c28da3d8854fbd8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.7 KB (396682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6ee65745809a5dc81b7ebcd048cd2b6cd69480d111ef08c012cb71a30996f9`

```dockerfile
```

-	Layers:
	-	`sha256:0ed97efaf6c383e4f6afcd2efdebca03303e9d6df61c0b9ba50b14e23e06ef10`  
		Last Modified: Fri, 18 Jul 2025 21:48:15 GMT  
		Size: 386.0 KB (385962 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:012108354c301b43e7b780cbf635ed4abd594cf23cae1a0b22593ebff1b6e240`  
		Last Modified: Fri, 18 Jul 2025 21:48:16 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fdf80a8916865a9cb737bbc04386529232106dbaca85aefc37cab4ff7935a3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161472516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47ed9633034573dd42097d58b69bbc20b6ce33b1f9904ad5526001485051e28b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Fri, 18 Jul 2025 19:06:54 GMT
ARG version=21.0.8.9.1
# Fri, 18 Jul 2025 19:06:54 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 18 Jul 2025 19:06:54 GMT
ENV LANG=C.UTF-8
# Fri, 18 Jul 2025 19:06:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 18 Jul 2025 19:06:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d02d07fda222ee822c634825bb45fa7a804b9bd3c8234251bbb38d689f3ade`  
		Last Modified: Fri, 18 Jul 2025 20:16:42 GMT  
		Size: 157.3 MB (157341766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7be941f58e5c349626e41101d71dac36518c0b6bf2d39c82ed9f5a439c7d4a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.3 KB (396301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fca14e8517f5a7cca3f856a6c6f947c751fd9afb3e4498baba8b4cffabc82952`

```dockerfile
```

-	Layers:
	-	`sha256:7adb3f8dd9e9285de9def89c2f2df280d15f8ccb96619aa1f7fb91b224a1cd72`  
		Last Modified: Fri, 18 Jul 2025 21:48:19 GMT  
		Size: 385.4 KB (385429 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5ada1c7e35612829f9f019c922c9072ccb9e92ce1695661cae73b384af2c874`  
		Last Modified: Fri, 18 Jul 2025 21:48:20 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
