## `amazoncorretto:8-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:6d20b0271fcb13972d46bdf5829476f40dc692385ed1c748136e52ea80d49d13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:edc8c02e3f1f55fd3322d21e1362c71b4fae05caa0c1cee3e60a5ca4e785ef99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104433450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:539330ef61a11683674f7ae289804c2134a35bbdfbfc0acf8e1f3a474dfed5ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:52 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:52 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:32:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad9c541c9de39e4501ab59df99f31a018f0d1449fc4495ca1e229141782ded9b`  
		Last Modified: Wed, 22 Apr 2026 21:33:06 GMT  
		Size: 100.8 MB (100786575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:dc1484d20dc67051522248a9be7658333a49ddca7b89c07bb602fec6578ba32f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 KB (260288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:365d1dab1351a925f747ca5c6ac62cd6b44d3b72f81f51ff29e4796b498890d8`

```dockerfile
```

-	Layers:
	-	`sha256:1f160715669ba9d4fd53727ce6c11cce7efa0e953f0f9e92847de3355c512b96`  
		Last Modified: Wed, 22 Apr 2026 21:33:04 GMT  
		Size: 250.9 KB (250933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4de55844a55d9b24b8d38a0f44c0bd1da668fd57688ba59f836c0d003a1924d2`  
		Last Modified: Wed, 22 Apr 2026 21:33:04 GMT  
		Size: 9.4 KB (9355 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ca63581c6ef6e579f2ea5c914cc60f10b71e04e001c35fabcf6760749259fcdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104565340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf943ba89f619199f2e58ead9d4862489edc3d1274b55260a459d41011565a7e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:32:49 GMT
ARG version=8.492.09.1
# Wed, 22 Apr 2026 21:32:49 GMT
# ARGS: version=8.492.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:32:49 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:32:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:32:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4686841dc5999838bd75e72515423fba75b966672569a7492e128a3a5a536db7`  
		Last Modified: Wed, 22 Apr 2026 21:33:04 GMT  
		Size: 100.6 MB (100570875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5867a001a8d2c2106e5afd5abb5f017ea5cbe2a47d28e07303cfb19a0ab0a039
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 KB (260524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2d1e4e2d9b92292c7f744dfa6cef2593975275eb98a190abc35d606020b2fb9`

```dockerfile
```

-	Layers:
	-	`sha256:526fc62ccdb72656666f5df0db3cebd750e50e8b9b405ac4bafc9281192f73fa`  
		Last Modified: Wed, 22 Apr 2026 21:33:01 GMT  
		Size: 251.1 KB (251065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:60dce4d3692401cf3a4d345bdd4f2ca8289573e914bc2edcab03e45f0e154e16`  
		Last Modified: Wed, 22 Apr 2026 21:33:01 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
