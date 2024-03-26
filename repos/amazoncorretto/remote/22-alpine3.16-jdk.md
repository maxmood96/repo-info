## `amazoncorretto:22-alpine3.16-jdk`

```console
$ docker pull amazoncorretto@sha256:e01eee194d87981bda6ece7c993c152c1bb51fe2f4cc6e6ebb476788e528709f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:22-alpine3.16-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fa2b083e68db6378ff33885ad83854fa20ebf2399e112ab4b347abd305fd3169
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.9 MB (160880178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:185347176e17acaa6a7aad3425f7301f9299ee8a659b28817f4adf10bdaa265c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 27 Jan 2024 00:31:09 GMT
ADD file:b308dfeecaa300a430b4e65e312a48eb5f191df7754e93ff4e7b2d04016b3ca7 in / 
# Sat, 27 Jan 2024 00:31:09 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 17:54:28 GMT
ARG version=22.0.0.37.1
# Tue, 26 Mar 2024 17:54:33 GMT
# ARGS: version=22.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Tue, 26 Mar 2024 17:54:34 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 17:54:34 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 26 Mar 2024 17:54:34 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a88dc8b54e91eb6b19695ef7e04865926d4df23004f414a3ee86978617492d4d`  
		Last Modified: Sat, 27 Jan 2024 00:31:53 GMT  
		Size: 2.8 MB (2807837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b90d8a90dde753218c8c6290b3413dbd0de3c832b512e8b56477fa301f77231`  
		Last Modified: Tue, 26 Mar 2024 17:58:43 GMT  
		Size: 158.1 MB (158072341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:22-alpine3.16-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b8e40e527f2d7a1eb39b969df70413ea4abb56e8de9995198137674c3fcdee4f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.1 MB (158120778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dac0912a13c73fd639c3dd263952574979ef24ad7092626076309fb1b5513cee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 26 Jan 2024 23:45:05 GMT
ADD file:0808047bc74f297cb13abd2ad67e5778ee4abaa5d69f2c5b133d11c0ce0e51aa in / 
# Fri, 26 Jan 2024 23:45:05 GMT
CMD ["/bin/sh"]
# Tue, 26 Mar 2024 18:07:14 GMT
ARG version=22.0.0.37.1
# Tue, 26 Mar 2024 18:07:21 GMT
# ARGS: version=22.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip
# Tue, 26 Mar 2024 18:07:23 GMT
ENV LANG=C.UTF-8
# Tue, 26 Mar 2024 18:07:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 26 Mar 2024 18:07:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:550f8bf8502cef18df2424ad36edbc4cc08c7ef11b44f493af59029aab98f61d`  
		Last Modified: Fri, 26 Jan 2024 23:45:48 GMT  
		Size: 2.7 MB (2708283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:777d590984d427e8e444999da6b614242e661fd82dbf907a45aa948f22238930`  
		Last Modified: Tue, 26 Mar 2024 18:11:39 GMT  
		Size: 155.4 MB (155412495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
