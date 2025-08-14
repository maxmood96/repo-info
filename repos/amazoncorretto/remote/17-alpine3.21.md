## `amazoncorretto:17-alpine3.21`

```console
$ docker pull amazoncorretto@sha256:76413c9b165c6b4f3a7e3737e3555cd20437cb7f858501cd7eb80bd9773f74d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:99aed2599274482f5813c4afb5b6165fb3af64796938bfa187c75221d084fe09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.7 MB (149664325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8740b67e070edc8b0957a05df20da7f9ae9d0be5913e3b515f6ef5491fa7bcb4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=17.0.16.8.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5719a46b40a13eef4133206d45eae6d6f3c03a84cdaa1f54626a618006bf03`  
		Last Modified: Wed, 16 Jul 2025 21:08:38 GMT  
		Size: 146.0 MB (146026755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:500eef2e1a3aeedb19c92ed6badf631ec7e5d553742808e16ddbd9c59d6de3f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 KB (396015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:061240929f0632bee9d1830c5e59a3057abab87deb9d976cc369b5f5e201cf2c`

```dockerfile
```

-	Layers:
	-	`sha256:857ac781f9e2900cacf8c6866fa6697e9a6c6ba9ecedf22574c66b14630fca6a`  
		Last Modified: Wed, 16 Jul 2025 21:48:49 GMT  
		Size: 385.3 KB (385290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d97407c68129bc67ed89367c7dd0c3940c1150263ae6a3096df02642d92dd41`  
		Last Modified: Wed, 16 Jul 2025 21:48:50 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f4bab578951baf60f08252aeb9cff396c0b03626281109a630971c7d5e1f5f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.3 MB (148307420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:059622e22f23dbe6e1700bf651ed74868a163396884cd9f33eaaa7e2b0a3f741`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=17.0.16.8.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=17.0.16.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9310cd728ad0ff1d784caa8919b50e63bfca95d7befaff2215c1ae28438dc3a4`  
		Last Modified: Thu, 17 Jul 2025 02:17:59 GMT  
		Size: 144.3 MB (144320483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:416b62286bef7efeb081753ad66137386779b87106a7bec317ca1e0e61567517
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **395.6 KB (395634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:304f7e1790c8ebfeab96dad8a495e5da8d1abbfb21cb15d79eceb515e4c11500`

```dockerfile
```

-	Layers:
	-	`sha256:617fc15b9a22df02397c5e0a16911dd36390fa53407a8770349f3d0be4c9853e`  
		Last Modified: Thu, 17 Jul 2025 03:48:44 GMT  
		Size: 384.8 KB (384757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9244e75190248bfad63698531d847ec0cf1983d0fc761f366a7c5146819664a6`  
		Last Modified: Thu, 17 Jul 2025 03:48:45 GMT  
		Size: 10.9 KB (10877 bytes)  
		MIME: application/vnd.in-toto+json
