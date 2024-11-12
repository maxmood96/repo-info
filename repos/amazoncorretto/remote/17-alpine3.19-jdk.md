## `amazoncorretto:17-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:0aca8021bc0ab4caced0447bd3b6f8649b575df9ad1edeacd0c43cc85b4939fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c1da5a967a290d541ede213717bdda9a7477c00e764df335370e70934d21df9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149069122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a87fa33b3c9c76ad5fda9dda73edd79debf3aa030e4480ee7311019d8ef40da`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a7cd7d9a21440da0d765f2989d75f069adf9b3463a765421a0590bca720920d4`  
		Last Modified: Mon, 09 Sep 2024 07:03:22 GMT  
		Size: 3.4 MB (3419728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:953e0ebb6a5e4c626886cf2d466ed1c31b470c97e3ccf6e10961ac876cca83ad`  
		Last Modified: Tue, 12 Nov 2024 02:12:21 GMT  
		Size: 145.6 MB (145649394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ed4fbd431b983850bca573a3b0ab014eb5992b39c6262d0b09975faf37fa725d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 KB (390946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95754356f60351a58e381c5f21da2a4f438f9caba7005454c00124c0f64e45b0`

```dockerfile
```

-	Layers:
	-	`sha256:fc50457e4505b926e95addeeb8b866b438915b194257acc3784f4afb24948c6a`  
		Last Modified: Tue, 12 Nov 2024 02:12:18 GMT  
		Size: 381.5 KB (381524 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc50d878f058afc031018cd8c549e9ee4a24537d8758a4d68b5244ad73ae10b0`  
		Last Modified: Tue, 12 Nov 2024 02:12:18 GMT  
		Size: 9.4 KB (9422 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6ae421a6d4e5cc8dc5155992a87d04acbfdd00cecfb59949a8f2978806c7b5ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147294267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56946c6d82f96ddcddc26b256cde29dfc57f7c64cbbb4e564c77569f59fcc49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:16 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Fri, 06 Sep 2024 22:44:16 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:7b14d02fba89363190724728cce94477c9ac8dc8143b677d29ba929a7cc3d6f3`  
		Last Modified: Wed, 16 Oct 2024 18:29:58 GMT  
		Size: 143.9 MB (143935164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a5b46edf420574261cf357240efe750aa64510a82d8342d4ba483590d10bfd20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.2 KB (390162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e68c99a38a4e4afd7df5c4e03037aa7a460035e9985255a84d9962500765b84`

```dockerfile
```

-	Layers:
	-	`sha256:3c7b0dc2fd7befc868c068111627d738b935821e5a94cfb4c527d9b7a1ed269e`  
		Last Modified: Wed, 16 Oct 2024 18:29:54 GMT  
		Size: 380.8 KB (380849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7977535722432fbda18b216c69ca7f4f86cd48e729f591ded9076b8651ac99e`  
		Last Modified: Wed, 16 Oct 2024 18:29:54 GMT  
		Size: 9.3 KB (9313 bytes)  
		MIME: application/vnd.in-toto+json
