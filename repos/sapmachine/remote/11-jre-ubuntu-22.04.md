## `sapmachine:11-jre-ubuntu-22.04`

```console
$ docker pull sapmachine@sha256:07bfb2b520b157f3079efb640629b8d2f9b8b6a009d4d6a98098d0b22845e399
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-22.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:7a83aacf59512502bf77cc11e7ec7529fae78653ecb67ca39fe8161a30208813
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.2 MB (79232216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d1df59efd77264911de19202cc28aa417c63cae7715dcebbdb5c83f6f84f7bd`
-	Default Command: `["bash"]`

```dockerfile
# Mon, 13 Oct 2025 17:23:18 GMT
ARG RELEASE
# Mon, 13 Oct 2025 17:23:18 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Mon, 13 Oct 2025 17:23:18 GMT
LABEL org.opencontainers.image.version=22.04
# Mon, 13 Oct 2025 17:23:20 GMT
ADD file:d025507456f1d7d19195885b1c02a346454d60c9348cbd3be92431f2d7e2666e in / 
# Mon, 13 Oct 2025 17:23:20 GMT
CMD ["/bin/bash"]
# Thu, 13 Nov 2025 23:40:20 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.29 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 13 Nov 2025 23:40:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 13 Nov 2025 23:40:20 GMT
CMD ["bash"]
```

-	Layers:
	-	`sha256:7e49dc6156b0b532730614d83a65ae5e7ce61e966b0498703d333b4d03505e4f`  
		Last Modified: Fri, 12 Dec 2025 19:57:37 GMT  
		Size: 29.5 MB (29536798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c30273f2e719b92c13d81ca14b1051f49d68bbd49700c039fce4a6baeb40d657`  
		Last Modified: Thu, 13 Nov 2025 23:40:40 GMT  
		Size: 49.7 MB (49695418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-22.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e0502f38a35e2672191a8661f676387a14754595a861f316118cebf8962e22d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fde13743404700e5443f3fcdadd575b7b762043a80fbd8471dc0c1940187e61`

```dockerfile
```

-	Layers:
	-	`sha256:70d436e4d24e530eb92f07400d9deb7beec24a53f5f96fa68a90efb9fd42ef16`  
		Last Modified: Fri, 14 Nov 2025 01:05:17 GMT  
		Size: 2.5 MB (2549886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6664e7367b710ccada6a3e97fa0a40f4788a74cb270509237b224e9d00aff339`  
		Last Modified: Fri, 14 Nov 2025 01:05:18 GMT  
		Size: 8.8 KB (8774 bytes)  
		MIME: application/vnd.in-toto+json
