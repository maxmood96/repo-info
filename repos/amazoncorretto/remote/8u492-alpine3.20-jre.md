## `amazoncorretto:8u492-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:768bd86fbad57b51b78193a6c4be1c4dc4f8cccec4e0bb48e0cc266ea21ffffb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3307698dbbed88de22fd63eee5a3870db8874fc094dd0a56cc145c483a4b0137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45381857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa2f404fc97adc5b847886bb72bb08e227f030539a621b4cfe9f6c54fba6abba`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:57:05 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:57:05 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:57:05 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:57:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca98eb94efbd61af5e7dfb69bbcd4e6bc2bdbae95c0a1ebb0cffc50570cbf13f`  
		Last Modified: Fri, 08 May 2026 22:57:15 GMT  
		Size: 41.8 MB (41751536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c117584e28ad0f060b8d365c2c97d92a4ab6768b61cc919caa3eb378113db176
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.5 KB (191474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:107fedb8056e44fcf41fab39d464efc2b56ab9ef54b3ec5557e06c4b9ea8839e`

```dockerfile
```

-	Layers:
	-	`sha256:4514f2a764f791a16f9e3c906592a732457d3434ad1a7048eb329f0701f67d92`  
		Last Modified: Fri, 08 May 2026 22:57:13 GMT  
		Size: 182.8 KB (182818 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4ad3571592b6572e0861022234f51793be51bc0eb925971e669f64d9a531c76`  
		Last Modified: Fri, 08 May 2026 22:57:13 GMT  
		Size: 8.7 KB (8656 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f5d7e0d62bc5031be79a79b0232d2035ca3ded9096bad6427eff933d2febd10f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45559048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb449338f0e1b6f084af7ba7c041f852e8300fe0d1cb498ac9b9119a81ef914e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:18 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:18 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:18 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f55fb334cff8f9e4056d5421343af5dba7a3c03feadcfaa2f3c3190e34fbf9`  
		Last Modified: Fri, 08 May 2026 22:48:28 GMT  
		Size: 41.5 MB (41466729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b0461245629ca454713af43cbd467988747cb975f45d84ffaae0a4cf3819bf83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.7 KB (191662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e770a382db6e3f1425afe5011f8e214aeddf193b740eca44dcbda688cdf0e140`

```dockerfile
```

-	Layers:
	-	`sha256:1201913b86e75b59d31075afb554a0aa03fd2de5a4c27e6051a102fe5c58f100`  
		Last Modified: Fri, 08 May 2026 22:48:27 GMT  
		Size: 182.9 KB (182926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8b9105e6caf1c9dc28d8d1d15055934350650fabb2f54ae737518be9a19ae20`  
		Last Modified: Fri, 08 May 2026 22:48:27 GMT  
		Size: 8.7 KB (8736 bytes)  
		MIME: application/vnd.in-toto+json
