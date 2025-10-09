## `amazoncorretto:21-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:29b224961c8064d9ce528a43af3b46c1c8c9a99e96c82a9afca303bab1559a5d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a649073ebdda94c5e967616342fd11a333bcf28bcf5f4b2e8eaabd4af96f0214
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.2 MB (163181838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16f232c4093da33505f133987cd4fde1ba68be4c2447b91e14cfe7634e2f66a1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3abd098eb11584626a85f0b70e78e75f2a2af9f0880291ae1a3a57e2edfc79e0`  
		Last Modified: Wed, 08 Oct 2025 23:41:19 GMT  
		Size: 159.4 MB (159379386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a81181e59c815d47e90b45311c94ff8b139fc4197eec5f9873d5c1479bacbaf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 KB (392481 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5ac902b7a27428468f9ebdcacee64173e0c99f4f9c8600813f55f794adb53a4`

```dockerfile
```

-	Layers:
	-	`sha256:aa32c03c1566fef991303e72cff94f97f598c59b4a8bef2bfa595b2e17cb6234`  
		Last Modified: Thu, 09 Oct 2025 00:49:39 GMT  
		Size: 381.8 KB (381762 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:327ef12bb24204c701e61ad248a13d74201664d65fa46d6ee98f2379e4c55ddb`  
		Last Modified: Thu, 09 Oct 2025 00:49:40 GMT  
		Size: 10.7 KB (10719 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:557f678d2fd8a841cc3bd5c454f95f0232df399ae4921114548f6b8b183c004d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161479306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14e6fb28f5ba11410fd768a20b2cdf8c05e0cd865a0d59d587ae672c662eb7f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=21.0.8.9.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8041dbcba7c8fd028d7049cfee4e9013b5a1e65e2d775eaf06f693f5a6ba5d`  
		Last Modified: Wed, 08 Oct 2025 22:58:51 GMT  
		Size: 157.3 MB (157341237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:043009a16c9bc55250c51b3dd482ae8ca7e852cd2327357e01456468cbdd5eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 KB (392100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17f14791721f9ebaacffaf4691347c98906282a7663be8882ca0ef76735664f1`

```dockerfile
```

-	Layers:
	-	`sha256:f9f20e928246b25068cec9d5c963e5d867f8d9f44b8b9725887019b6c4587403`  
		Last Modified: Thu, 09 Oct 2025 00:49:43 GMT  
		Size: 381.2 KB (381229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b590ef1200da25b2ef02eecd92993b498fff53908d3f3114f06b4367c32483`  
		Last Modified: Thu, 09 Oct 2025 00:49:44 GMT  
		Size: 10.9 KB (10871 bytes)  
		MIME: application/vnd.in-toto+json
