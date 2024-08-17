## `sapmachine:22-jre-ubuntu-jammy`

```console
$ docker pull sapmachine@sha256:a0e5473ab326f837eb69bbfd3e49a2cec66197e2444f121b1b5a1e3e2d98def7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-ubuntu-jammy` - linux; amd64

```console
$ docker pull sapmachine@sha256:fb64a099dcf006e5260130027169847320360564e54f5513c38d38b282d0987f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **88.7 MB (88667125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b496d4a0163b468860ff73b0f2917444b3e655cffbecb3c5bcd7ac35f209e19f`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 27 Jun 2024 20:10:10 GMT
ARG RELEASE
# Thu, 27 Jun 2024 20:10:10 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 27 Jun 2024 20:10:10 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 27 Jun 2024 20:10:12 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Thu, 27 Jun 2024 20:10:12 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:3713021b02770a720dea9b54c03d0ed83e03a2ef5dce2898c56a327fee9a8bca`  
		Last Modified: Thu, 27 Jun 2024 20:18:28 GMT  
		Size: 29.5 MB (29534055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294f9501cb8f5b078c020494fa079a1acca96f6276094d0e5b92cb47602de299`  
		Last Modified: Fri, 19 Jul 2024 17:59:06 GMT  
		Size: 59.1 MB (59133070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:920535e6b026382ccc10ef1cc121c76b86b615e3bf93fe7ce4c0a4e35d8ab100
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2399250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f526e2d5f3b3e6b647dc664687fc2a6324fbf7f500375ea0a01ac4b52952ea7c`

```dockerfile
```

-	Layers:
	-	`sha256:6803ea10bd7a7e2c6c6dde1aac44766f6f3e1eb2155075ea1a70e45af8697946`  
		Last Modified: Fri, 19 Jul 2024 17:59:05 GMT  
		Size: 2.4 MB (2390040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a786ba7edcdb38359b7e4a4cb769dabf84d8f21f803241e1e6c6e667d36083cd`  
		Last Modified: Fri, 19 Jul 2024 17:59:05 GMT  
		Size: 9.2 KB (9210 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-jammy` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:9c3f0ff029c02082a037d430704694203e15c0b66d65cbc8ce9834bf4cc877b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.5 MB (85493922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea35bbbd10afb09439bb313b78312232ad6359423326abdd7f1c90422400dd6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:4126c5ecc7750c7d2beb8c08d15aea03d96910453b36d2fb2d41185fdca7b20f in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:e63ce922f0229bde5aea9f366c46883dcd23747e7d2c541f16665f199dbf98b8`  
		Last Modified: Tue, 13 Aug 2024 10:44:55 GMT  
		Size: 27.4 MB (27358683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f4560712663f0c5236a3a9963035a8d5fd5c5f89b104e4f44011cad54ab4112`  
		Last Modified: Sat, 17 Aug 2024 04:10:01 GMT  
		Size: 58.1 MB (58135239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:36a607f67bd027ab647e98a16a23904f69f8bd5615c9725e9e9e40cd11985e08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:381e42677701b2703ec1bba9d587d62afa66ed205977dff6b3a5d90064a504e0`

```dockerfile
```

-	Layers:
	-	`sha256:607552cd1efdb9b167cca51c9e40291b83b93bbee106d9dd8ef86e253d9444ca`  
		Last Modified: Sat, 17 Aug 2024 04:09:59 GMT  
		Size: 2.4 MB (2389113 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:570a0bfbd47e607843c2c108a564125303cae6045eb5442f4da58b0b79c57948`  
		Last Modified: Sat, 17 Aug 2024 04:09:59 GMT  
		Size: 9.5 KB (9535 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-jammy` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:a234f11ff19e30529d4932525bdf9a63ffac414377e1fc8047281c3c3c7b786c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.0 MB (95038223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a5fca14eba1db947d7af06bbe016e0967b0cf58f992385a8d11e3fe130b4a09`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 18 Jul 2024 15:16:23 GMT
ARG RELEASE
# Thu, 18 Jul 2024 15:16:23 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 18 Jul 2024 15:16:23 GMT
LABEL org.opencontainers.image.version=22.04
# Thu, 18 Jul 2024 15:16:23 GMT
ADD file:c9b0fd1ddcc2e70c763a44be7034882e75f36c79435448061c7785f0f01476db in / 
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["/bin/bash"]
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:593b8356181268f4632d882f9f41d8b565910ac10009886043617c157fbfcae6`  
		Last Modified: Tue, 13 Aug 2024 10:45:08 GMT  
		Size: 34.5 MB (34464178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:983bae52bd13176cbc0bbbeb6b92ac478580b4cf1457a3c8d477438be909273b`  
		Last Modified: Sat, 17 Aug 2024 02:35:56 GMT  
		Size: 60.6 MB (60574045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-jammy` - unknown; unknown

```console
$ docker pull sapmachine@sha256:9c764283d20024a9eb68de5a05e98d7e796abb495b055ab432d18e99e280f264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3708bbaec256e293af87d8335d904f4314d95c93fd0e92ddf956f72313877786`

```dockerfile
```

-	Layers:
	-	`sha256:c8434e8e45579bc1b793035948920fdc707d256714b18dea39f19516d05d9920`  
		Last Modified: Sat, 17 Aug 2024 02:35:54 GMT  
		Size: 2.4 MB (2393400 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6644fcff84dd80b3fe1961e01d1f764a14c692dbd7f36c314fac56507e059ea`  
		Last Modified: Sat, 17 Aug 2024 02:35:54 GMT  
		Size: 9.3 KB (9260 bytes)  
		MIME: application/vnd.in-toto+json
