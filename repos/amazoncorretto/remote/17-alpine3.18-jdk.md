## `amazoncorretto:17-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:2d5b506f91d65c0a8ab43873bef3f90230d0756b97a18ee219e0c3eb0deffd93
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3b449c2bcce9e80b79588cc7d05de711fd5c24fa6afaeb0222bf395d9806e90f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149096162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e6ebc05ba382967739adb35f8d041d437ca0aa7d5e11e4cd116ca61b68beb4c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f54a5150a7602eaef3169b83e73d5927b20aef2fcaefcba18b532bd63b328fff`  
		Last Modified: Tue, 14 Jan 2025 20:33:01 GMT  
		Size: 3.4 MB (3417974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:393e08a13995b6c73297e7f4e8d45ea50e2b51617f9932fc11a9bcadfe1ec98f`  
		Last Modified: Tue, 04 Feb 2025 04:55:14 GMT  
		Size: 145.7 MB (145678188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7f7e10187dbe2a05566ac9876d06135c14340d26fed67b8babc14936ff463303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e085191f1cbcb3923c9ea93d4fbc26892e23268922696e2e55fe9c7ccb074895`

```dockerfile
```

-	Layers:
	-	`sha256:1b84908451219ed7d203d2e46b6bd30ab4475120634b6240367d1c29ffa14add`  
		Last Modified: Thu, 23 Jan 2025 18:27:16 GMT  
		Size: 380.2 KB (380234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09831773f7659531628be0b8c2ca5ec073ea5b78450295cb554bb193e4093442`  
		Last Modified: Thu, 23 Jan 2025 18:27:16 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b09e5a1ece6edf4bc237511efa5b29963bee1a32bcd5a869d5769686f758696a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.4 MB (147363472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b1e8679c3a976aae6f2bf6089c45d6931bd93e555f027f58184ed8bd4cb178`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7dd969e575ab8b667fb8f4eac8523e001318acccef7d68d1d05b2a9bcf221d`  
		Last Modified: Wed, 05 Feb 2025 11:01:36 GMT  
		Size: 144.0 MB (144021611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:458635b34c7a2781907a57d6abab009f320cf0bc1d2886a91b0ab66bb8a265da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.2 KB (389174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97f85f750cb3d3d9bb8da7f7896e344ad2aec77aaf8a1b6e9f64fccb8cad58e1`

```dockerfile
```

-	Layers:
	-	`sha256:916ed097b9a76130590bc96b7fdf5d2ce356f0026b0b712bf923ef9b29bf4461`  
		Last Modified: Thu, 23 Jan 2025 18:47:39 GMT  
		Size: 379.7 KB (379653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9abb240bc996db7b519d0e4c2870cf0541532b6928744ecdef24571b21e8d5f7`  
		Last Modified: Thu, 23 Jan 2025 18:47:39 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
