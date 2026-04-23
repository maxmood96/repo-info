## `amazoncorretto:25-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:ebfdf4c4ccab378d2bc2fb775d45c53149116a9f91f85316577a912476e1f40d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d40addafcdc1a11e44fd85ce436f0ed1fc2be28ebf050f073f17b5ffa88d5056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.6 MB (184619008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16863c4676719f3438dc29f0da23d14fb83d652c5d78f718057007d2102a2647`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:19 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:19 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:19 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8788edd38f9acd2e8164f2b7924c94cca73ed5739a2813794ebf448396133389`  
		Last Modified: Wed, 22 Apr 2026 21:35:41 GMT  
		Size: 181.0 MB (180988687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:420ef86ba0a838708744de5fad203d8749e125fcfe2bae2a22c2fa71ea47ec2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.7 KB (599668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bf11991dfd7445ff5e88a51a15acd85eb3edc7d90ea3f6df0d84d0e49677311`

```dockerfile
```

-	Layers:
	-	`sha256:cc27d4869fe556c6ef8b5d2c7247f5d0d23f15646b1fe941b56e127199639239`  
		Last Modified: Wed, 22 Apr 2026 21:35:36 GMT  
		Size: 590.3 KB (590297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5c53127213000e14586e46f502f84ed85cab615733023b1337937e82e57872d5`  
		Last Modified: Wed, 22 Apr 2026 21:35:36 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:44db83d6f1d72549979e628ae3ef3dc2166fea2c4fe0350d4773b4d8f34144fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182719126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c39019f189de40d81cdcea50d7a2d32e6db9237e1e3878157b05323884371f9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:16 GMT
ARG version=25.0.3.9.1
# Wed, 22 Apr 2026 21:35:16 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:16 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a447d14cb6af637eeb62516137d1f2a463433d80070785465ec4291172c73560`  
		Last Modified: Wed, 22 Apr 2026 21:35:39 GMT  
		Size: 178.6 MB (178626807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c1abb0823e416458d0ab3ea59673a58b0bf42d682c3629bfd3d7ca8fc19cef1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.2 KB (599186 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:101be92f5538a7d9c08fc90c711909afd59b632f2d2edc68d706281e2ff4d1ed`

```dockerfile
```

-	Layers:
	-	`sha256:919ebc2c330486c8768cb65ac006b8bd2233257f2deba1c70729cfffed5e497e`  
		Last Modified: Wed, 22 Apr 2026 21:35:34 GMT  
		Size: 589.7 KB (589713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b95bb269135191bc5832c637e4fefaee8f6eb50f924e52140f730a062e2229cf`  
		Last Modified: Wed, 22 Apr 2026 21:35:34 GMT  
		Size: 9.5 KB (9473 bytes)  
		MIME: application/vnd.in-toto+json
