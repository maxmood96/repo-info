## `amazoncorretto:25-alpine-full`

```console
$ docker pull amazoncorretto@sha256:32d81edae73e1670244827c2f12e5bcf0d335f035b538455fe9d02eb0771d41b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:acaf9f3006d0069fc1f16bd8507785b93f630311dbcd23d50b8f5b616d2f4a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184868725 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d4965dd753f4bf5afcf1ef518eddd7ba04b9e587b2eb07bc953c701d7f12768`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:29 GMT
ADD alpine-minirootfs-3.24.1-x86_64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:29 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:19:33 GMT
ARG version=25.0.3.9.1
# Tue, 16 Jun 2026 00:19:33 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:19:33 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:19:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:19:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:55afa1ecc21d2bb5e5045f32dafee56272ffd89860bac26f6c32123439af26a4`  
		Last Modified: Sun, 14 Jun 2026 06:44:06 GMT  
		Size: 3.8 MB (3846391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff9cb0a96d2f74fba017aa19f46fb759c77128dec9f0557f4bbf9fc25bfa3c8d`  
		Last Modified: Tue, 16 Jun 2026 00:19:53 GMT  
		Size: 181.0 MB (181022334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4692f07dd760edcb40064db6b6962fff1803defcb9e957ad52bde8fd891a9594
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **603.6 KB (603554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9314b3d6e5b350e2f71d2da0941a5d49bb5d925c771bf023ba8f12ab6294b276`

```dockerfile
```

-	Layers:
	-	`sha256:cae3aad7f1fc3f6de83740934d55e96dae0af7c949e6d5b1e70a834f3792bfd2`  
		Last Modified: Tue, 16 Jun 2026 00:19:48 GMT  
		Size: 592.9 KB (592877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4510965dc9573f881b35a0bfde71ba630e7c7723f32e9eec113e948dc8edf918`  
		Last Modified: Tue, 16 Jun 2026 00:19:48 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:da20e1e0a2004dfb95e963d6ad978b5c0effdfc7000bce6a68836058ef24b427
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182820722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79650cc130b4c054f668e9e0111027dda65008b7774a167b9ec8953a669c7d3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jun 2026 00:01:20 GMT
ADD alpine-minirootfs-3.24.1-aarch64.tar.gz / # buildkit
# Tue, 16 Jun 2026 00:01:20 GMT
CMD ["/bin/sh"]
# Tue, 16 Jun 2026 00:17:44 GMT
ARG version=25.0.3.9.1
# Tue, 16 Jun 2026 00:17:44 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jun 2026 00:17:44 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jun 2026 00:17:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jun 2026 00:17:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5de55e5ef9c033997441461efe7ba23a986db059c0bb78b38f84ee0d72b99167`  
		Last Modified: Sun, 14 Jun 2026 06:44:31 GMT  
		Size: 4.2 MB (4183037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5726ab05b71301a574d768553ef460fcff02a1878fcbbeeba8bab6803a367df0`  
		Last Modified: Tue, 16 Jun 2026 00:18:06 GMT  
		Size: 178.6 MB (178637685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b41800f30b09c264e59d57968d3b4d49a623a105293f7bf9e7a5fc0f8fdde38e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.5 KB (602520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23e7a4861ca3c45ae0ef0002d88ebf7b5b569f9b7b1fc0508d44b9d66ea0ba98`

```dockerfile
```

-	Layers:
	-	`sha256:c350ddd4f736903a59de757419be3e7968a29116d77adafe621f244b98158bea`  
		Last Modified: Tue, 16 Jun 2026 00:18:02 GMT  
		Size: 591.7 KB (591691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:17d18faa59c2fa7cb2eb3a9da4ad4fb345d3fb6323b0d38353993eff050a27ef`  
		Last Modified: Tue, 16 Jun 2026 00:18:02 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.in-toto+json
