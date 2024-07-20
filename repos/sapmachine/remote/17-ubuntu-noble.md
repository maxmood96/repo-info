## `sapmachine:17-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:ba8ed815e62079178f291e996f02de240666ac8656178d951ca3d6dabc999749
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:17-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:346da42a84a7f5a25dc14cc04184b35a7fe9bc7787dba9e33b3575ab4e5c20c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **230.1 MB (230134900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50824a861e99603269fdc973d57db5c9885124630c444537acc84e3c712125ce`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c027fc52595e534c43532679a8ea4fc3b94b2e251ca581dd0e3e82c3ffd8003`  
		Last Modified: Fri, 19 Jul 2024 18:00:38 GMT  
		Size: 200.4 MB (200429747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:2bdb69bde54aecbca4b3d670a09e2777426a097db876bbd646b1ad9df2a974c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2456302 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07e8da48f9e1a33f504fe1c077424b91211791915f87873f309231ddf1ff5534`

```dockerfile
```

-	Layers:
	-	`sha256:bf594421dcdbbdf056317c3601df6f283de18da9bd699a03be425546e757a94d`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 2.4 MB (2445162 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c44a9102536371cd38a129f65aa2af01480e40faa3f842cd5b4177696c485136`  
		Last Modified: Fri, 19 Jul 2024 18:00:33 GMT  
		Size: 11.1 KB (11140 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:5ff6a7e6afeb5f62099df7e74df4deaa61595eb1cf081d0d6ed91812f6818215
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **227.9 MB (227923443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a122638b91202281ebe266d67e248dbf46d5e32199f9a736ba6360f05a51b53e`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82c294a72089bd50d34b77cd5357637d854bef87dbaf9c5d064c33777c235ed`  
		Last Modified: Sat, 20 Jul 2024 00:21:27 GMT  
		Size: 199.1 MB (199080400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:1ed971e28bc6fcafc7cf0169715c4cea0f0184c25c88772a3b87b700694bb7b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2457262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58cd3d93aa3e04115f78ca07f3e343a9a943cf00cb84c7054d18e61712634519`

```dockerfile
```

-	Layers:
	-	`sha256:9456aba26010e27f4b1566bddd1b5b53d6a952f30a2de6cd5524d2c30c979508`  
		Last Modified: Sat, 20 Jul 2024 00:21:23 GMT  
		Size: 2.4 MB (2445725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:776249113d1a3d819f479956097701ef5a03d9099d6ca8a074b1e252f9e9548b`  
		Last Modified: Sat, 20 Jul 2024 00:21:22 GMT  
		Size: 11.5 KB (11537 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:17-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:eb08a09595ecd7c87b8f745edbce5cbdabf6cd3e853471969c084e83ca8cd862
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.1 MB (236146629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a532cad7d492a63f1e7cbe63198fe45215b56210239c01db4e88ead7e2c918`
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
# Thu, 18 Jul 2024 15:16:21 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.12     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 18 Jul 2024 15:16:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b12d0af8d60badb7234998f99df29af68d4095d1f8096d597191912640b1002`  
		Last Modified: Fri, 19 Jul 2024 23:31:19 GMT  
		Size: 201.6 MB (201640600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:17-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:212d0bbb32c675fba380117b584ce1dede6591d7d57808c738930aba84eb003a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2458424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9effeeb752045c3d08dd8dbeb995ccb28458bfb953937dff0297098676cafabc`

```dockerfile
```

-	Layers:
	-	`sha256:91e3d866c4a5ca78816d4f2eb66e521fc5f636c91b2b5de285fbe63b54bc7bcd`  
		Last Modified: Fri, 19 Jul 2024 23:31:14 GMT  
		Size: 2.4 MB (2447198 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0a455a3983301b2772137c161ead0750121f6655a90dacf9e3c9285a7f1461f`  
		Last Modified: Fri, 19 Jul 2024 23:31:14 GMT  
		Size: 11.2 KB (11226 bytes)  
		MIME: application/vnd.in-toto+json
