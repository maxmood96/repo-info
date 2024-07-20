## `sapmachine:22-jre-ubuntu-noble`

```console
$ docker pull sapmachine@sha256:5260dd238bf262c87f898b37bddfb5d773f1a2887acd6c0b2ca743a46543a7fa
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown

### `sapmachine:22-jre-ubuntu-noble` - linux; amd64

```console
$ docker pull sapmachine@sha256:91e0f39e905c9a2b673ac3fd2405fde693ea9973f55a5c1016c2e91e34634d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **89.2 MB (89215111 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8902f6d367d17e01b10aca6d1ab31813e328e03c0f411175134a03618ba1faf4`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:9c704ecd0c694c4cbdd85e589ac8d1fc3fd8f890b7f3731769a5b169eb495809`  
		Last Modified: Fri, 07 Jun 2024 12:11:26 GMT  
		Size: 29.7 MB (29705153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d2283ad9c8833701e7a83547a4e809f1223c30a58026c81f08a82ce6238b2a5`  
		Last Modified: Fri, 19 Jul 2024 17:59:01 GMT  
		Size: 59.5 MB (59509958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:71b1d3f59dfd373446c0dd37d801283f38a78ed04e40a58f707b8f1d14b772d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2373862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76579578ae83bbcdbb16b38aab0bd0b74588b340a1fbe5676c45c65a6cdf166b`

```dockerfile
```

-	Layers:
	-	`sha256:6bc6f6261b9c7eb63c7a8f7ce88288e341a25b6876e01b73bcea481f9bb876dd`  
		Last Modified: Fri, 19 Jul 2024 17:59:00 GMT  
		Size: 2.4 MB (2363691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:02a502c015bdf4aeabbae7481aab10f782c9cd8abf0f6467839895b0ccc5740c`  
		Last Modified: Fri, 19 Jul 2024 17:59:00 GMT  
		Size: 10.2 KB (10171 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-noble` - linux; arm64 variant v8

```console
$ docker pull sapmachine@sha256:ed1bc4884724822d78102f16c0ee8295ea14fe374ac57cb3bfa303b2f379bedb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **87.4 MB (87415293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dd0ad34a45c6e925ad4a07a79217346bb5c3df4104b8208d36604bfd42f1937`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:eed1663d223832f23c8ca8fc0f9b48e2bcb0813b94a692d43b0a0a963e89d20f`  
		Last Modified: Fri, 07 Jun 2024 12:11:33 GMT  
		Size: 28.8 MB (28843043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b084d1ea6ad66dbde16f748591cb97b509fb137b85274854da223c01a51c05a`  
		Last Modified: Fri, 19 Jul 2024 23:58:12 GMT  
		Size: 58.6 MB (58572250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:8dffa217a2858065114d06370b9949e18cea172e53fef47187d88848c3ce4554
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9aff345de88693ef47a8b08454a6be2e3677a211f3fa8c24f968f7dabc489b`

```dockerfile
```

-	Layers:
	-	`sha256:a0c500a7d387e6bef9abf7e845a2286a7b3f4fc495d9b8e93da9f033d3ea75ac`  
		Last Modified: Fri, 19 Jul 2024 23:58:10 GMT  
		Size: 2.4 MB (2363587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ad336562422ec10de8b06c811178949801147734b3cfe5b900b4716fba93716`  
		Last Modified: Fri, 19 Jul 2024 23:58:10 GMT  
		Size: 10.5 KB (10533 bytes)  
		MIME: application/vnd.in-toto+json

### `sapmachine:22-jre-ubuntu-noble` - linux; ppc64le

```console
$ docker pull sapmachine@sha256:8438d1795675ea5e0757e2f8a3f5817355dd99f0d45e69c3e369bf0cb0edae95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **95.6 MB (95598312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb4ebd6f4edb7dbe66ef502ae316bd3d05de4fd40fcbc8affac4c1601b0fd059`
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
# Thu, 18 Jul 2024 15:16:23 GMT
RUN apt-get update     && apt-get -y --no-install-recommends install ca-certificates gnupg     && export GNUPGHOME="$(mktemp -d)"     && gpg --no-default-keyring --keyring gnupg-ring:/etc/apt/trusted.gpg.d/sapmachine.gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && chmod 644 /etc/apt/trusted.gpg.d/sapmachine.gpg     && echo "deb http://dist.sapmachine.io/debian/$(dpkg --print-architecture)/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-22-jre=22.0.2     && apt-get remove -y --purge --autoremove ca-certificates gnupg     && rm -rf "$GNUPGHOME" /var/lib/apt/lists/* # buildkit
# Thu, 18 Jul 2024 15:16:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-22
# Thu, 18 Jul 2024 15:16:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:875c01bc1b3e6b966440b42d40365968bfdd742c762026b5739c5d1f493510d7`  
		Last Modified: Fri, 07 Jun 2024 12:11:45 GMT  
		Size: 34.5 MB (34506029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19d522f5f2d793e04ee07d7549bfdb692c572db1c57b5e58cd1e1617db2668a5`  
		Last Modified: Fri, 19 Jul 2024 22:52:56 GMT  
		Size: 61.1 MB (61092283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `sapmachine:22-jre-ubuntu-noble` - unknown; unknown

```console
$ docker pull sapmachine@sha256:88ce0b5d4f115f05ac0ef3ba621f0d19444a1781ad141b3c61e03ac5546e39c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377267 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f9f077cdb45c16a610d2cbb278fbc364d0ad6e51c2fbb8681f3c5f6b49da42`

```dockerfile
```

-	Layers:
	-	`sha256:ecde113b75e01ace681afbd34482d5554e13bf4e66b842c645a60db9a993dc99`  
		Last Modified: Fri, 19 Jul 2024 22:52:54 GMT  
		Size: 2.4 MB (2367027 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8e5ad4af3a48737f393b41b65a1f3c041ba339f99bc2987b6fce46592f76d95`  
		Last Modified: Fri, 19 Jul 2024 22:52:54 GMT  
		Size: 10.2 KB (10240 bytes)  
		MIME: application/vnd.in-toto+json
