## `sapmachine:21-jre-headless-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:69899fad8b42e7f7bca924e4801246a9ec20a544bb9ad54d87173c3370d50150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:3d8fd7db96652922e72db91f96bac93a6aa38ab54947ebe5fd1425e11ae5fc6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.8 MB (88846741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:958f896581cd1f660379d9852010237ad10f45aa3f14fcd89599d6791c82731b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:06 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:06 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:06 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:08 GMT
ADD file:5601f441718b0d192d73394b35fd07675342837ec9089ddd52dd1dc0de79630e in / 
# Fri, 07 Jun 2024 12:00:09 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26f33c9db92523acaa27ac6562e59c86087858df90084e8a9cd970e24e617d95`  
		Last Modified: Fri, 19 Jul 2024 18:00:12 GMT  
		Size: 59.1 MB (59141588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:e537c21fabf635fbd58e6d75b0e5cafde53ebca51646c4987b5754e85822096d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2137440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e67d0d6b39c827efe13c54e8dc4e66f81397f8098555569d090385811e617a`

```dockerfile
```

-	Layers:
	-	`sha256:232437f512984513abe65b1c23321c1854e8a71a3c574dced9c3e875433b95c2`  
		Last Modified: Fri, 19 Jul 2024 18:00:11 GMT  
		Size: 2.1 MB (2127043 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686b51044d30b4356c201f59a682c6975cfd1ee45f19d4d77c4d9556c3d025cc`  
		Last Modified: Fri, 19 Jul 2024 18:00:10 GMT  
		Size: 10.4 KB (10397 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:84a46f76f301fca36ff13a87adfe798f5b8d3af13d9b5c455a30d42b5d5e4dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.1 MB (87085484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dacbc239597854a3adaff65b1f6ae28c4dce24c138b98f4c4dc1fb82e7366b1`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 11:48:27 GMT
ARG RELEASE
# Fri, 07 Jun 2024 11:48:27 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 11:48:27 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 11:48:32 GMT
ADD file:9018302bda8cbdb55f2f84a40373c46413db64611139a450dbfec3fc55b8e6ea in / 
# Fri, 07 Jun 2024 11:48:33 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9b34745ffce7a7070c2a629916532bab80d6196649bb3b788f3d7dec2544670`  
		Last Modified: Sat, 20 Jul 2024 00:11:40 GMT  
		Size: 58.2 MB (58242441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:a301c85d6e7cc4075c137eeddb16f7c647cbb31b75d987450beb6a67e136c3c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2138319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b818339e1845ee9a0a63da53f50b422448c13738bfec5210bdd068452b20ea2`

```dockerfile
```

-	Layers:
	-	`sha256:f9d69c1ac82668524b73df14fab88733aaff58e7f8f0f1f35c1fa04566d8b429`  
		Last Modified: Sat, 20 Jul 2024 00:11:38 GMT  
		Size: 2.1 MB (2127561 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e9b9ac258aa082f968e297f6e4d546de45082ecb0b8eeb6df05c410dc545b63`  
		Last Modified: Sat, 20 Jul 2024 00:11:38 GMT  
		Size: 10.8 KB (10758 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:21-jre-headless-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:474d1606332a881b7bfaf377a70ac844224d4e55877ae0e020a1241c03075fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.1 MB (95141026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fdfc9b11a205b9d4d067a9d1862a00716838ae671485346c3a1f02da1df8a9b`
-	Default Command: `["jshell"]`

```dockerfile
# Fri, 07 Jun 2024 12:00:24 GMT
ARG RELEASE
# Fri, 07 Jun 2024 12:00:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Fri, 07 Jun 2024 12:00:24 GMT
LABEL org.opencontainers.image.version=24.04
# Fri, 07 Jun 2024 12:00:28 GMT
ADD file:e767a66d1508f3628411abaff75d39ed1d6261596c668fa88252ed9a584e7fa4 in / 
# Fri, 07 Jun 2024 12:00:29 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:16 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-21-jre-headless=21.0.4     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-21
# Thu, 18 Jul 2024 15:16:16 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72ddc9c45f5b9a57e4434dd500f472b4045992de0100ee8f341388f22aa32216`  
		Last Modified: Fri, 19 Jul 2024 23:15:58 GMT  
		Size: 60.6 MB (60634997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:21-jre-headless-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:31379e0ee2c5f9def94045e41fbe9e289283d59b37c6146c907671ae1c875dbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 MB (2141411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6498f703826d2f324e47bdfe6dcc714d93becf82003eb1d3b1bc4e2682e05ae`

```dockerfile
```

-	Layers:
	-	`sha256:7908c2b45e039c70255b71bc572a551ce252538e05a829c1f7f304ac10d48e95`  
		Last Modified: Fri, 19 Jul 2024 23:15:55 GMT  
		Size: 2.1 MB (2130947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a58ffb596881b33aeb99e7eff96b5e2f780fb509e492c9033a48e7b6f05d574`  
		Last Modified: Fri, 19 Jul 2024 23:15:54 GMT  
		Size: 10.5 KB (10464 bytes)  
		MIME: application/vnd.in-toto+json
