## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:9b9068b38301043ab5f8e71b7a28d3362c550edf5a40ba92f6238e95479a0ad0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3f619ab465ef218e1b865ac8ba5503a113000cfde5d7d9bdd3aae83c35b92661
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **144.8 MB (144777178 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32bd7fc0c4e0110303c76e15816c1619a4e420a58b34a84449b3b819b7f2cb84`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:33:24 GMT
ARG version=11.0.20.9.1
# Thu, 28 Sep 2023 23:33:31 GMT
# ARGS: version=11.0.20.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Thu, 28 Sep 2023 23:33:32 GMT
ENV LANG=C.UTF-8
# Thu, 28 Sep 2023 23:33:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 28 Sep 2023 23:33:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:198630ea96142bcc184915dc1faf35392959b5b73b651ed0f644710b394bb6d6`  
		Last Modified: Thu, 28 Sep 2023 23:38:05 GMT  
		Size: 141.4 MB (141375211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:115971f3f0a6fc2ae0138871062ad596a5182637b3a0eb0f2e5c835384ce6d95
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.0 MB (142977645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:476620519e7dba18b1a2aa98dccec7b7271c93a653b442fd0bf08035e3062e4f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Fri, 08 Sep 2023 21:45:13 GMT
ARG version=11.0.20.9.1
# Fri, 08 Sep 2023 21:45:17 GMT
# ARGS: version=11.0.20.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip
# Fri, 08 Sep 2023 21:45:18 GMT
ENV LANG=C.UTF-8
# Fri, 08 Sep 2023 21:45:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 08 Sep 2023 21:45:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:487691ba44bd14168fd612cbd37ababe78e0a9422495b0164fff5a71dbf27479`  
		Last Modified: Fri, 08 Sep 2023 21:55:11 GMT  
		Size: 139.6 MB (139646878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
