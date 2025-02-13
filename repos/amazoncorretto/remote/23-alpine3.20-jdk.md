## `amazoncorretto:23-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:a87888924d462a842c6bd84c0d9ae1da7653827d3dd346cb9f4dba53aa16834e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f1cbfa4fc0cff3b55713027ef1fae1c3c8556f7bf475b768212b43f35d78056
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170313566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bae178b352bda7fac8233c865b773d05f945a02989dcb4f129a9dbfa0e619bc8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:586601369655864cd8664041a64a90e1b83d320f2f7c255ecc58d4384aefa9c1`  
		Last Modified: Mon, 03 Feb 2025 20:40:54 GMT  
		Size: 166.7 MB (166687306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d6725765559f65bf9241f8585c5f75990bdf11c7c9290d672c4db6f13bb3eb6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 KB (390533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e855de8070cb51833f6bf370e9eea7fc4d1f1d3772fbbd509d5e73298f5264b4`

```dockerfile
```

-	Layers:
	-	`sha256:9134215d61d69b2af6d2a376cc467e116e8e371a3b70df9b8bb3c9b13a5fb393`  
		Last Modified: Thu, 23 Jan 2025 18:27:44 GMT  
		Size: 379.8 KB (379813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0df5a11473cb5430fdfc0eab878558a3181a16648d3c9c0167c35b10fe07ead1`  
		Last Modified: Thu, 23 Jan 2025 18:27:44 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f7cecdbe7afd06a602939ce5f752c98d410b5275af01a63e995da45a3ed7fc58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.5 MB (168499098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad217f369e068d1d1b0cb1624b4e88727cae6ee84a0d55d736121d4fb1985bde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d8a1b77d8fb2973a5165487ae4f9ba602b01b62aa495d03847f6a44857d4e29`  
		Last Modified: Wed, 05 Feb 2025 21:10:56 GMT  
		Size: 164.4 MB (164408329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9f497379153d4b2d17d23733d71efab3acc457311085a6f5f703d16cbded59a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389512 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60d504997fc7f392da24efb1858731e42546dc2a3edb27b77ef0dc353b7095e4`

```dockerfile
```

-	Layers:
	-	`sha256:83bd24864454e5d987103d23111264bddb1153b7426aa74e461152eaa6db612a`  
		Last Modified: Thu, 23 Jan 2025 18:58:14 GMT  
		Size: 378.6 KB (378640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0629dc887c1bf7f9da378b1f7ef9d1e15a4d010d304cd6ae1cba8adee5707e41`  
		Last Modified: Thu, 23 Jan 2025 18:58:14 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
