## `sapmachine:11-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:174fa7dc8e5594ec331816b0df8153f4e674e05056182c6be54e960ba91c5299
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:0b86f039536094345d5c07785509a9ffd8dcbc68c157301dafe24025b76aded8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.5 MB (79544043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2a22f520be2e2bad9804137ab4b0c298c89e9c5d6d141cca29d2698fc88f49d`
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
ADD file:32d41b6329e8f89fa4ac92ef97c04b7cfd5e90fb74e1509c3e27d7c91195b7c7 in / 
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
	-	`sha256:af6eca94c8104c8e90d3f9efe59c2b3a02b20aad3d985e31c7cd009ea104c447`  
		Last Modified: Wed, 01 Oct 2025 10:09:45 GMT  
		Size: 29.5 MB (29536818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77ae5e92a5d9b7e0c62c041c45a9ac12088a7bfba0c74754007422e811b269a7`  
		Last Modified: Thu, 02 Oct 2025 05:21:01 GMT  
		Size: 50.0 MB (50007225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:f284342a97940ec9b94787b4a8cb2803e388fc3ad8745bab55b18f840124ceb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2558703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aebba9efb5243a2b2b4e3d5128a00e9e8ee84ffea9180ab9cc33f33ae814a891`

```dockerfile
```

-	Layers:
	-	`sha256:195cfd16122f3df0d1d7b876dcdaf24fb2101664fa52a490d085b87657c5b4ba`  
		Last Modified: Thu, 02 Oct 2025 09:05:08 GMT  
		Size: 2.5 MB (2549886 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7e5d076735029232e13ff10871ea6a138e956db40338e6a146d8628a0cb3765`  
		Last Modified: Thu, 02 Oct 2025 09:05:08 GMT  
		Size: 8.8 KB (8817 bytes)  
		MIME: application/vnd.in-toto+json
