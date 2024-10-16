## `amazoncorretto:23-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:8f4d0b648cb8ff430b745b838052db068a5b8a48fb6b5d27043b2c45c0da6d0b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7bb88648765d67a1824417a383bcc6f379648a7357effad8ba3dd46cb3aac1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170078276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5414e31b713d8e0c4a9b5fb89f65f3c80211293df25533ac1b8ded13875c90a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:13 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Fri, 06 Sep 2024 22:20:13 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d5dff81a40e966461fc05ad904b4bb216dfce83f9d2a0f3679eb100d2650d75`  
		Last Modified: Wed, 16 Oct 2024 17:57:32 GMT  
		Size: 166.7 MB (166658570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9015b5c28917136cd82f6ed12bdff38bcf6432aa8359830f4c4a196db4836fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.5 KB (392482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c89a9fa98c79ffb5fbbd99e9c161e07361226f8e0a76a5dab2fb9ee0f2abb4b8`

```dockerfile
```

-	Layers:
	-	`sha256:c47ac571a981e9e277a956ef67992fbdac9853f5db25d834fcadeaaf9424a641`  
		Last Modified: Wed, 16 Oct 2024 17:57:30 GMT  
		Size: 383.3 KB (383276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d1b09d64f6d66ca1dd0c4e8d799aee8395205332cf1d92ec5bbc4079817d53c`  
		Last Modified: Wed, 16 Oct 2024 17:57:30 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d47fc44209a5fbfc053e30d8b6206dd90dc0e5e0be97b7a66ad0b2e83dddcc83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167712219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:890302e0facfc5ee20fbd5964e829f084f0f43106250280e3ba4d461cf225a86`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2dd93f82e0da47365900af0b6971963089f4ecd2b3fb9ef4edb84f05acedf6b`  
		Last Modified: Wed, 16 Oct 2024 18:45:29 GMT  
		Size: 164.4 MB (164353116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cc630a99253080a52b21626f3f438ffb49b7046d736e7fefe501962212361dc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.4 KB (391358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:189d4e6ce6e12041a5cc43171b9c2a0f08b1913d51e0d0acbb9ecfe49e1569bc`

```dockerfile
```

-	Layers:
	-	`sha256:ad19453817c87d6b0fe4f5441c568d8e56e4c91bba1280db3dd85b74bc8bb1f5`  
		Last Modified: Wed, 16 Oct 2024 18:45:25 GMT  
		Size: 382.1 KB (382053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0336723148e8be1fb0f917cb912cd16af89d24cd7e196c2e7da8a53d93ccd9`  
		Last Modified: Wed, 16 Oct 2024 18:45:25 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json
