## `amazoncorretto:25-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:1828ee4c02cf4c3567ac7e64e55e79a7b74f36ac5bed0e52d8b2af1883a189ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:27aeade44716adfe9a75746be5010c2a95f862416e49fabacb4e6bed267ece9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.4 MB (184381645 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcf20eb96f6b3b76719db9d1715db53005ee60d1ab4d849e622b180e905fb356`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:59 GMT
ARG version=25.0.2.10.1
# Fri, 17 Apr 2026 00:22:59 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:59 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:59 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8b7c49a86eff21b1946c2436b76ed49b0e94c184a5079792ba2b2982561eab4`  
		Last Modified: Fri, 17 Apr 2026 00:23:20 GMT  
		Size: 180.8 MB (180751324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b40f3fdb7e2d007d49a770d4a62b5efe3b0d5264610f3540d6657958b5dd37b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 KB (599027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5a9afdb2cd29cabb5dec412def39d443e8d63bbda9ca74a3bdfd3c23ad83525`

```dockerfile
```

-	Layers:
	-	`sha256:f1e754a780d72ff887eb14737d0f8fea3ca886c303a687bbc6197ffb9b97029c`  
		Last Modified: Fri, 17 Apr 2026 00:23:16 GMT  
		Size: 589.7 KB (589655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:539d4c2ad0d7be7ceee1960b06a2c401c7a6686b48125d010f10e959b33ef6eb`  
		Last Modified: Fri, 17 Apr 2026 00:23:16 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f534d034b1f92ee98044396d56b148b93ba08dbe2697ba80d4b7d2478a79efcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182508677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0feed1579d5806ac0ba8bea0013a3d2733511bc3cf5dc121d8ae547c248f8dc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:09 GMT
ARG version=25.0.2.10.1
# Fri, 17 Apr 2026 00:25:09 GMT
# ARGS: version=25.0.2.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:25:09 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:25:09 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:25:09 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61a2f881ea1b8d3ca880662ddf79a3d751c5e79fb82bcd5f1ac65b5e456d6b9e`  
		Last Modified: Fri, 17 Apr 2026 00:25:30 GMT  
		Size: 178.4 MB (178416358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:523f0cc4a43282fbe0634e0a6ab9b947d159c4342b754cb54d896c07e40a5ace
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be37c789db2c94f1fdc10fcf5996e37f4002f31c2d7585b42b32726dc6989523`

```dockerfile
```

-	Layers:
	-	`sha256:d65aee2075d61127716ebf2f41c18300b75efbdf917846f43f683086626e0d6a`  
		Last Modified: Fri, 17 Apr 2026 00:25:26 GMT  
		Size: 589.1 KB (589071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2218ed37b45dfe11b594645b188440064796a6e6f47c8591d64082d5ff8ff50a`  
		Last Modified: Fri, 17 Apr 2026 00:25:26 GMT  
		Size: 9.5 KB (9476 bytes)  
		MIME: application/vnd.in-toto+json
