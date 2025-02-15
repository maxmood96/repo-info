## `amazoncorretto:8u442-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:d74a655abd38ba7ae850a6be8f7f2e9af37acd25ef19722b397b47d45f1523c4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:23aaf5068e534616eb530ca2ef1e9177a0ad00d63a400f51aa4ab5e0b910c4ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103866695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c07301d54d0ab38970261421ebeb5fe41edef881629f367fc3a3a6faf87cda7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17bc2b72ec1b58aebe6bed023c31857d1e015e516b47df0719cf919e75337d80`  
		Last Modified: Fri, 14 Feb 2025 20:36:29 GMT  
		Size: 100.2 MB (100224448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eafc3e2cda43b25fdff1b399a83b2b56392dbf84feec264d345f02f29f78af0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 KB (259122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d7f8c89a9652990259d030d21947178f26d79cb3e397a0f303dcc5950740fe7`

```dockerfile
```

-	Layers:
	-	`sha256:b4ec3ced5b0a6f06b84ac269ddfd2cc0dcc3328df4e8da710cc47d1f8c67429d`  
		Last Modified: Fri, 14 Feb 2025 22:49:41 GMT  
		Size: 248.4 KB (248426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f1e2e1f906de8347a92f821101bb14393d6e6926e9631f870660e442af15175`  
		Last Modified: Fri, 14 Feb 2025 22:49:41 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b7969629aeb0fbee0fbb417c8cea38b8e41363023caf8b1e684a320360afd65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104002010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c02a383ed396132eea39554cbb46be7f362893087591b7a9fbc86e6aa8204363`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:210cb7d0b4eaadfd241f7597434fe45c8b95829d5e7ff916d7532a9cb82745cd`  
		Last Modified: Sat, 15 Feb 2025 09:07:12 GMT  
		Size: 100.0 MB (100008981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:359140ebffc18a51aca6f2fcf311ddcf7004fdae0d940a961b5ffd60520c8f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 KB (259454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5df2e28f7e140571cd20d0165cba2894646a9eea677eac114b9298784a9105b5`

```dockerfile
```

-	Layers:
	-	`sha256:b641d644d8bcb77ed85fd7ad715fca20fae0279b42fe188ab2daff5ded63df78`  
		Last Modified: Sat, 15 Feb 2025 01:49:37 GMT  
		Size: 248.6 KB (248606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:938546d72cf978b3ebcf6178b3a0ac41f38f74dc390b515b9cf1cdf753d62e06`  
		Last Modified: Sat, 15 Feb 2025 01:49:38 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
