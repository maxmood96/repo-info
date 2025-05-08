## `sapmachine:11-jre-ubuntu-24.04`

```console
$ docker pull sapmachine@sha256:422b9bfc4c8899bdd2c17399bbe165c93ff1846a7ccbd6e2a255bfb0592608bc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `sapmachine:11-jre-ubuntu-24.04` - linux; amd64

```console
$ docker pull sapmachine@sha256:a79e1a9a65cdf662c1af29786f79b44571a16ff053f1966a048e031abb5f90f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.1 MB (80104476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b259409b11618188456036671a43cbe2c5f254d265cf17fade7957a432e1598`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 16 Apr 2025 10:34:44 GMT
ARG RELEASE
# Wed, 16 Apr 2025 10:34:44 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Wed, 16 Apr 2025 10:34:44 GMT
LABEL org.opencontainers.image.version=24.04
# Wed, 16 Apr 2025 10:34:44 GMT
ADD file:ad85a9d7b0a74c2140bd51d9c4559cca392991e0c95f84cb139347348e5d1f9a in / 
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["/bin/bash"]
# Wed, 16 Apr 2025 10:34:44 GMT
RUN apt-get update &&     apt-get -y --no-install-recommends install ca-certificates gnupg &&     export GNUPGHOME="$(mktemp -d)" &&     gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23 &&     chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg &&     echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list &&     apt-get update &&     apt-get -y --no-install-recommends install sapmachine-11-jre=11.0.27 &&     apt-get remove -y --purge --autoremove ca-certificates gnupg &&     rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Wed, 16 Apr 2025 10:34:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Wed, 16 Apr 2025 10:34:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:0622fac788edde5d30e7bbd2688893e5452a19ff237a2e4615e2d8181321cb4e`  
		Last Modified: Thu, 08 May 2025 17:04:41 GMT  
		Size: 29.7 MB (29717529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c3df1cfc3c57db76ec97981359c740fdffd7a4253dcd4403a718786dada6f25`  
		Last Modified: Thu, 08 May 2025 21:20:57 GMT  
		Size: 50.4 MB (50386947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:11-jre-ubuntu-24.04` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2e2b8c421ae33cfc4aa986089b20a1a32857c09a6c783245c8cf14cf9f47a335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5579bc55335464cc86a2c492f2845877b574138681cbc99580639d5be4f9f41f`

```dockerfile
```

-	Layers:
	-	`sha256:ba9b63b84710058d24c0b01c1ae4ad0bf5124f861e3cd680334571331c1277bc`  
		Last Modified: Mon, 05 May 2025 16:37:12 GMT  
		Size: 2.4 MB (2391606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ddda6403b157c3b29808b26fedd0b35d29c9e88e0c136228cc1e6352d7f5907`  
		Last Modified: Mon, 05 May 2025 16:37:12 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
