## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:2c2e22fab4d0c543967011407bb20ca16fec40b113b02a999ba4a1dd388ac723
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:4027e81f8fc67e1ddd6ce7f459f7ee321006f291366a703c92b8f8a75436ea24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:822cdbd490d1f31f9b4bf045454ab5c14b0882882356af9a7f326d77c522e0ff`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 11 Aug 2025 06:09:39 GMT
ARG RELEASE
# Mon, 11 Aug 2025 06:09:39 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 11 Aug 2025 06:09:39 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 11 Aug 2025 06:09:39 GMT
ADD file:9303cc1f788d2a9a8f909b154339f7c637b2a53c75c0e7f3da62eb1fefe371b1 in / 
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["/bin/bash"]
# Mon, 11 Aug 2025 06:09:39 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.28 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 06:09:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Mon, 11 Aug 2025 06:09:39 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:60d98d907669dc22e547405da3e409eb14496606f4ac90692c5f2ef5081c4b1e`  
		Last Modified: Tue, 19 Aug 2025 19:22:51 GMT  
		Size: 29.5 MB (29536935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1748fbd4725d8b89d0cdc037b9d3c51832ae3eea1c7612682cae9e53f857f7e9`  
		Last Modified: Wed, 17 Sep 2025 17:41:29 GMT  
		Size: 50.0 MB (50007109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ffc91f1c0a9b7c2378ab7389f0856ea88d480466e1084184a8a8270602a0307
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50985323cdaf174c1dd8ad89b50a587ff9aee640eb052b934c9e6b4de1c8c3b9`

```dockerfile
```

-	Layers:
	-	`sha256:22dab822778d748109e5171ea1b1f9a1a7b59130d06f39eaa6c0556c5fe69c57`  
		Last Modified: Wed, 17 Sep 2025 21:04:42 GMT  
		Size: 2.5 MB (2549886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb16a4e451a5fd3154dab39c0a0bf259118d36201dde6dfa0dbfe25535b4d287`  
		Last Modified: Wed, 17 Sep 2025 21:04:43 GMT  
		Size: 8.8 KB (8817 bytes)  
		MIME: application/vnd.in-toto+json
