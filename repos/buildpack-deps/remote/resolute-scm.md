## `buildpack-deps:resolute-scm`

```console
$ docker pull buildpack-deps@sha256:c34fa930a4dcc0df28eb462dde3a213234317bf21fd43411ff80bfae1ef5dc55
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v7
	-	unknown; unknown

### `buildpack-deps:resolute-scm` - linux; arm variant v7

```console
$ docker pull buildpack-deps@sha256:279f2a0b0d962793642fec6d201dabfc9aa0804ad6298193d99532d13798e9a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.4 MB (99378872 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d91cd904193b7f6d6ecf0006478a2e4c55ca911a0f6e1ab2355dac6dbed7fa64`
-	Default Command: `["\/bin\/bash"]`

```dockerfile
# Mon, 03 Nov 2025 16:29:08 GMT
ARG RELEASE
# Mon, 03 Nov 2025 16:29:08 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 03 Nov 2025 16:29:08 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 03 Nov 2025 16:29:08 GMT
LABEL org.opencontainers.image.version=26.04
# Mon, 03 Nov 2025 16:29:18 GMT
ADD file:b5205c826c7c3a6374a9466a98138ed499f3832207208fa02f5929bd90a79717 in / 
# Mon, 03 Nov 2025 16:29:18 GMT
CMD ["/bin/bash"]
# Fri, 14 Nov 2025 01:02:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 14 Nov 2025 01:08:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	apt-get dist-clean # buildkit
```

-	Layers:
	-	`sha256:a4edfc31f2f766770f61ea46a0f4f1fd53dacedd2336abb49820c8c4368e9405`  
		Last Modified: Thu, 13 Nov 2025 23:03:49 GMT  
		Size: 31.8 MB (31756944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ebd3cc0b0d366216373a9d97fee336363125c0fb40eaf46a136ed5b085c17f`  
		Last Modified: Fri, 14 Nov 2025 01:02:39 GMT  
		Size: 17.0 MB (17043524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a330e9013ab0e736ac9941a3f10a187cdd8455d91096aef8b896682f821ccf3`  
		Last Modified: Fri, 14 Nov 2025 01:09:04 GMT  
		Size: 50.6 MB (50578404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `buildpack-deps:resolute-scm` - unknown; unknown

```console
$ docker pull buildpack-deps@sha256:8047f47a22f574b655cdefcd3cce49da94917068a46138f1108e9370802a5f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5761608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:786e466f3900ea3617a43395c2d8c57485279bacd9c88952743e52ddfa03eb3d`

```dockerfile
```

-	Layers:
	-	`sha256:aac6e3a0c2648a41c70e83f59c07cec5bbd39d9076f56fd90a29a7dc0011ee64`  
		Last Modified: Fri, 14 Nov 2025 02:21:35 GMT  
		Size: 5.8 MB (5754263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:199774efc4f361dc10352af81a1ff6b92e9fb6b5bda643f1f650db95edb998ca`  
		Last Modified: Fri, 14 Nov 2025 02:21:36 GMT  
		Size: 7.3 KB (7345 bytes)  
		MIME: application/vnd.in-toto+json
